##################################
This page is about Basic syntax
##################################

*********
Sections
*********

見出し文字の下に以下の記号文字のいずれかを**見出し文字の数より多く**並べる（アンダーラインとして並べる）ことで、ドキュメントの各セクション（見出し）を作成できます。

::

  ! " # $ % & ' ( ) * + , - . / : ; < = > ? @ [ \ ] ^ _ ` { | } ~

これらの内特に以下を利用することが推奨されます。

::

  = - ` : . ' " ~ ^ _ * + #



例::

   #########
   大見出し
   #########

   本文

   **********
   中見出し
   **********

   本文

   ========
   小見出し
   ========

   本文

↓

.. image:: imgs/section-sample.png

::

   注意：
   ・ 見栄えを良くするためにオーバーラインを書くこともできます。（見出しの上に並べる事ができる）
   ・ オーバーラインを記述する場合はアンダーラインと同じ文字数で書く必要があるようです。
   ・  Section用文字は以下の順序で利用することが推奨されているようです
     1. #
     2. *
     3. =
     4. -
     5. ^
     6. "

*****
List
*****


::

   * This is a bulleted list.
   * It has two items, the second
   item uses two lines.

   1. This is a numbered list.
   2. It has two items too.

   #. This is a numbered list.
   #. It has two items too.

↓

* This is a bulleted list.
* It has two items, the second
  item uses two lines.

1. This is a numbered list.
2. It has two items too.

#. This is a numbered list.
#. It has two items too.


****************
Literal blocks
****************

::

   This is a normal text paragraph. The next paragraph is a code sample::
   
      It is not processed in any way, except
      that the indentation is removed.
   
      It can span multiple lines.
   
   This is a normal text paragraph again.

↓

This is a normal text paragraph. The next paragraph is a code sample::

   It is not processed in any way, except
   that the indentation is removed.

   It can span multiple lines.

This is a normal text paragraph again.


****************
Doctest blocks
****************

:: 

   >>> 1 + 1
   2

のように **>>>** と記述するとデコレーションされます

↓

>>> 1 + 1
2

****************
Tables
****************

テーブルの表記方法にはいくつかあります。


グリッドテーブル表記
====================

::

   +------------------------+------------+----------+----------+
   | Header row, column 1   | Header 2   | Header 3 | Header 4 |
   | (header rows optional) |            |          |          |
   +========================+============+==========+==========+
   | body row 1, column 1   | column 2   | column 3 | column 4 |
   +------------------------+------------+----------+----------+
   | body row 2             | ...        | ...      |          |
   +------------------------+------------+----------+----------+

↓

+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
| (header rows optional) |            |          |          |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | ...        | ...      |          |
+------------------------+------------+----------+----------+

シンプルテーブル表記
====================

::

   =====  =====  =======
   A      B      A and B
   =====  =====  =======
   False  False  False
   True   False  False
   False  True   False
   True   True   True
   =====  =====  =======

↓

=====  =====  =======
A      B      A and B
=====  =====  =======
False  False  False
True   False  False
False  True   False
True   True   True
=====  =====  =======


csv-tableディレクティブ表記
===================================

::

   .. csv-table::
      :header: "AAA", "BBB", "CCC"
      :align: left

      a,b,c
      1,2,3

↓

.. csv-table::
   :header: "AAA", "BBB", "CCC"
   :align: left

   a,b,c
   1,2,3

list-tableディレクティブ表記
==============================

::

   .. list-table:: Frozen Delights!
      :widths: 15 10 30
      :header-rows: 1

      * - Treat
      - Quantity
      - Description
      * - Albatross
      - 2.99
      - On a stick!
      * - Crunchy Frog
      - 1.49
      - If we took the bones out, it wouldn't be
         crunchy, now would it?
      * - Gannet Ripple
      - 1.99
      - On a stick!

↓

.. list-table:: Frozen Delights!
   :widths: 15 10 30
   :header-rows: 1

   * - Treat
     - Quantity
     - Description
   * - Albatross
     - 2.99
     - On a stick!
   * - Crunchy Frog
     - 1.49
     - If we took the bones out, it wouldn't be
       crunchy, now would it?
   * - Gannet Ripple
     - 1.99
     - On a stick!

************
Hyperlinks
************

リンクの書き方は主に2つあります

::

   This is a paragraph that contains `a link`_.

   .. _a link: https://domain.invalid/

↓

This is a paragraph that contains `a link`_.

.. _a link: https://domain.invalid/

::

  `Link text <https://domain.invalid/>`_

↓

`Link text <https://domain.invalid/>`_

*******
Images
*******

画像を利用したい場合はimageディレクティブを利用します。
画像の場所は、該当のrstファイルからの相対パスと、トップのソースディレクトリからの絶対パスのいずれも利用できます。

::

   .. image:: imgs/sample1.jpg
      :width: 50 %
      :align: left

↓

.. image:: imgs/sample1.jpg
   :width: 50 %
   :align: left

**********
Footnotes
**********

* \[\#name\]\_ と  .. [#name]　を書くことで脚注を記述できます
* nameは省略しても良いです。(\[\#\]\_だけでも可で、自動採番されます。)
* #ではなく数字をそのまま記述しても良いです。


::

   Lorem ipsum [#f1]_ dolor sit amet ... [#f2]_

   .. [#f1] Text of the first footnote.
   .. [#f2] Text of the second footnote.

↓

Lorem ipsum [#f1]_ dolor sit amet ... [#f2]_

.. [#f1] Text of the first footnote.
.. [#f2] Text of the second footnote.


.. note:: html生成時は **rubric** ディレクティブを書く事で脚注についてそれらしい整形がされますが、PDF生成時は変な感じになるので書かない方が良さそうです。


**********
Citations
**********

* 引用、参考文献の記述方法です。
* 書き方はFootnote(脚注)と似ています。
* このように [参考文献名ABC]_ (\[参考文献名ABC]\_)と、それに対応するディレクティブを以下のように書いておくと、自動的に参考文献ページが巻末に生成されます。

::

  .. [参考文献名ABC] 2020 CDE著 FGH文庫

.. [参考文献名ABC] 2020 CDE著 FGH文庫

.. warning:: PDF生成ではそれらしい感じになりますが、HTML生成での利用はおすすめしません。