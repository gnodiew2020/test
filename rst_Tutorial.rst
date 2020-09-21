======================
 | reStructuredText |
======================
**这是一个用于练习的文件**

*emphasis*

**strong**

``literal``

term (up to a line of text)
   
   Definition of the term, which must be indented

   and can even consist of multiple paragraphs

next term
   Description.


This is a normal text paragraph. The next paragraph is a code sample::

   It is not processed in any way, except
   that the indentation is removed.

   It can span multiple lines.

This is a normal text paragraph again.

简单表格
^^^^^^^^
======  ======  ========
A       A       A and B
======  ======  ========
False   False   False
False   True    False
True    False   False
True    True    Ture
======  ======  ========

格子表格
^^^^^^^^

+----------------------+----------+----------+----------+
| Header row column 1  | Header 2 | Header 3 | Header 4 |
| (Header rows option) |          |          |          |
+----------------------+----------+----------+----------+
| body row 1, column 1 | column 2 | column 3 | column 4 |
+----------------------+----------+----------+----------+
| body row 2           | ...      | ...      |          |
+----------------------+----------+----------+----------+

外部链接
^^^^^^^^

`Link Text <http://example.com/>`_

=================
This is a heading
=================

.. function:: foo(x)
              foo(y, z)
   :module: some.module.name

   Return a line of text input from the user.

.. image:: gnu.png
   (options)

Lorem ipsum [#f1]_ dolor sit amet ... [#f2]_

.. rubric:: Footnotes

.. [#f1] Text of the first footnote.
.. [#f2] Text of the second footnote.

.. function:: foo(x)
              foo(y, z)
   :module: some.module.name

   Return a line of text input from the user.

.. image:: gnu.png
   (options).. 

.. |caution| image:: warning.png
             :alt: Warning!
