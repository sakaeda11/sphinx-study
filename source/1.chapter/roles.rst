.. _sample-target:

##################################
This page is about Roles
##################################

::

    :rolename:`content`

のように記述しrole名によって定められた意味・修飾を **content** に対して行う。

* 注意
    * contentを囲む"\`"は必須
    * \:rolename\:の後にスペースを入れない
* \:rolename\:を記述せず、\`content\`のみ記述した場合はデフォルトのロールとして処理される
    * デフォルトのロールは\:title-reference\:となっている模様
    * 以下のように **default-role** ディレクティブを利用することでデフォルトロールは変更可能

::

    .. default-role:: subscript

例えば

::

    :emphasis:`強調`

    :strong:`強調`

    :literal:`リテラル`

    :subscript:`下付き文字`

    :superscript:`上付き文字`

    :title-reference:`書籍、定期刊行物などのタイトル`

    `デフォルトのロール`

↓

:emphasis:`強調`

:strong:`強調`

:literal:`リテラル`

:subscript:`下付き文字`

:superscript:`上付き文字`

:title-reference:`書籍、定期刊行物などのタイトル`

`デフォルトのロール`

のようになる

*******************************************************
Cross-referencing syntax
*******************************************************

================
ref
================
ドキュメント内の自由な位置に対してクロスリファレンス(リンク)を作成できます。

* refによるクロスリファレンスの記法は2通りあります。


記法1::

    .. _my-reference-label:

    Section to cross-reference
    --------------------------

    This is the text of the section.

    .. _my-figure:

    .. figure:: whatever

       Figure caption

    It refers to the section itself, see :ref:`my-reference-label`.

* セクションのタイトルの直前や、図の直前にラベルを記述し、\:ref\:\`label-name\`と記述する方法です。
* ラベルはユニークである必要があります
* ラベルは\_(アンダースコア)で始まる必要があります。

記法2::

    :ref:`Link title <sample-target>`

* このようにラベル名を別名にすることもできます。

------------------
refの例
------------------

:ref:`sample-target`

:ref:`figure-reference`

:ref:`Link title <sample-target>`


================
any
================

anyというロールは、最初に標準のクロスリファレンス doc, ref, option として解釈できるか試し、
それで見つからなければ使われている全てのドメインのオブジェクト(ターゲット)に参照できるか試します。

::

    :any:`sample-target`

↓

:any:`sample-target`


便利ですが、明示的にrefなどを利用した方が良いように思います。


*******************************************************
Others
*******************************************************


::

    Since Pythagoras, we know that :math:`a^2 + b^2 = c^2`.

    :abbr:`LIFO (last-in, first-out)`

    :command:`cp abc.txt def.txt`

    :dfn:`abc ABC 123 あいう`

    is installed in :file:`/usr/lib/python2.{x}/site-packages`

    :guilabel:`&Cancel`

    :kbd:`Control-x Control-f`

    :mailheader:`Content-Type`

    :make:`abc`

    :manpage:`ls(1)`

    :menuselection:`Start --> Programs`

    :program:`example.exe`

    :regexp:`[0-9a-z].`

    :samp:`print 1+{variable}`

    :pep:`8#id15`

    :rfc:`3986#section-2`

↓

Since Pythagoras, we know that :math:`a^2 + b^2 = c^2`.

:abbr:`LIFO (last-in, first-out)`

:command:`cp abc.txt def.txt`

:dfn:`abc ABC 123 あいう`

is installed in :file:`/usr/lib/python2.{x}/site-packages`

:guilabel:`&Cancel`

:kbd:`Control-x Control-f`

:mailheader:`Content-Type`

:makevar:`abc`

:manpage:`ls(1)`

:menuselection:`Start --> Programs`

:program:`example.exe`

:regexp:`[0-9a-z].`

:samp:`print 1+{variable}`

:pep:`8#id15`

:rfc:`3986#section-2`