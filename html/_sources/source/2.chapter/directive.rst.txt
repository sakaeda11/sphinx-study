##################################
This page is about Directive
##################################

*****************
toctree nest
*****************

toctreeは入れ子にすることができます。

.. toctree::

   AAA BBB CCC <subpage/sub1>
   subpage/sub2

************
note
************

.. note::

   ".. note::"というディレクティブを記述した場合このようになります。

***********
warning
***********

.. warning::
   ".. warning::"というディレクティブを記述した場合このようになります。

***************
admonition
***************

::

   .. admonition:: テストです

      あいうえお

↓

.. admonition:: テストです

   あいうえお


*************
math
*************

数学記号を記載したい場合

::

   .. math::

      (a + b)^2 = a^2 + 2ab + b^2

↓

.. math::

   (a + b)^2 = a^2 + 2ab + b^2


**********
todo
**********
conf.pyに以下の設定をした上で利用できます。

conf.py::

   extensions = [
   'sphinx.ext.todo',
   ]

   todo_include_todos = True

::

   .. todo:: なにかしらのTODO1


   .. todo:: 

      なにかしらのTODO2

↓

.. todo:: なにかしらのTODO1


.. todo:: 

   なにかしらのTODO2



************
todolist
************

ドキュメント全体からtodoを探してリストアップしてくれます。


::

  .. todolist::

↓

.. todolist::