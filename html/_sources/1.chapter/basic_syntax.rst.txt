This page is about Basic syntax
==================================

**List**

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


**Literal blocks**

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


**Doctest blocks**

:: 

   >>> 1 + 1
   2

↓

>>> 1 + 1
2

**Tables**

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

https://docutils.sourceforge.io/docs/ref/rst/directives.html#csv-table

::

   .. csv-table::
      :header: "AAA", "BBB", "CCC"
      :widths: 15, 10, 30

      a,b,c
      1,2,3

↓

.. csv-table::
   :header: "AAA", "BBB", "CCC"
   :widths: 15, 10, 30

   a,b,c
   1,2,3

**Hyperlinks**

This is a paragraph that contains `a link`_.

.. _a link: https://domain.invalid/

`Link text <https://domain.invalid/>`


**Sections**