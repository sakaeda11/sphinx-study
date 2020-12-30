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