====================
 |reStructuredText|
====================
-------------------------------------------------
 Docutils_ 标记语法及解释器
-------------------------------------------------

:Date: $Date: 2016-05-24 13:48:37 +0200 (Di, 24. Mai 2016) $

.. Note:: "reStructuredText" 是 **一个** 单词, 不是 *两个*

.. contents::

reStructuredText 是一个易于阅读、 所见即所得的纯文本标记语法解释系统。
对于把内联程序文档快速创建成简单的网页和独立文档非常有用（比如：Python docstrings），

reStructuredText 用于设计特定应用程序域的可扩展性，
其解释器是 Docutils_ 的一个组件。

reStructuredText 是对轻量级标记系统 StructuredText_ 与 Setext_ 的修订与重新注解。

reStructuredText 的最初目的是为 Python Docstrings 及其它文档域定义实现并实现一套标记语法。
使其简单易读且超强通用。标记的预期目的是将 reStructuredText 文档转换为有用的结构化数据格式。

完整了解Python模块的示例，使用reStructuredText记录请看 statemachine.py_


用户文档
========

- `A ReStructuredText Primer`__ (HTML file, or `text source`__).
- `Quick reStructuredText`__ (user reference)
- `reStructuredText Cheat Sheet`__ (text only; 1 page for syntax, 1
  page directive & role reference)

Users who have questions or need assistance with Docutils or
reStructuredText should post a message to the Docutils-users_ mailing
list.

__ docs/user/rst/quickstart.html
__ docs/user/rst/quickstart.txt
__ docs/user/rst/quickref.html
__ docs/user/rst/cheatsheet.txt
.. _Docutils-users: docs/user/mailing-lists.html#docutils-users


文档参考
============

- `An Introduction to reStructuredText`__ (includes the Goals__ and
  History__ of reStructuredText)
- `reStructuredText Markup Specification`__
- `reStructuredText Directives`__
- `reStructuredText Interpreted Text Roles`__

__ docs/ref/rst/introduction.html
__ docs/ref/rst/introduction.html#goals
__ docs/ref/rst/introduction.html#history
__ docs/ref/rst/restructuredtext.html
__ docs/ref/rst/directives.html
__ docs/ref/rst/roles.html

开发者文档
===========

- `A Record of reStructuredText Syntax Alternatives`__
- `Problems With StructuredText`__

__ docs/dev/rst/alternatives.html
__ docs/dev/rst/problems.html


如何做
--------

- `Creating reStructuredText Directives`__
- `Creating reStructuredText Interpreted Text Roles`__

__ docs/howto/rst-directives.html
__ docs/howto/rst-roles.html


试试在线
=============

If you want to try reStructuredText out without downloading Docutils, you
can play with the "simple online editor for reStructuredText" on
http://rst.ninjs.org/


感言
======

The following testimonials are excerpts from unsolicited posts to
mailing lists and the comp.lang.python newsgroup.  Being excerpts,
there's often context missing, which sometimes tones down the message.

`Ueli Schlaepfer on Doc-SIG, 2002-03-28`__:

__ http://mail.python.org/pipermail/doc-sig/2002-March/002526.html

    I have adopted reST as my tool of choice for producing notes while
    doing lab work (mostly in a matlab environment).  Since then, the
    quality of such documentation has increased noticeably, mostly for
    two reasons:

    - I no longer need to switch to another tool, so the threshold has
      fallen to very low.  Note that "another tool" means Winword...
    - Still, I have a powerful set of markup constructs at my
      fingertips that let me create the kind of documents I need with
      more ease than any other tool I can think of.

    Thanks to reST/DPS [now Docutils --ed], I'll soon be able to go
    ahead and apply the same tools for extracting documentation out of
    my Python code.  Hey, that's a printable and a browsable version
    *for free*!  Personally, I consider this a large benefit.

    ... All essential constructs for everyday use are there, and much
    more if needed. ...

`Guido van Rossum, enthusiastic about PEP 287 but a bit hasty (see the
follow-ups) on Python-Dev, 2002-04-02`__:

__ http://mail.python.org/pipermail/python-dev/2002-April/022131.html

    Good PEP, David!  What's the next step?  Should the processing
    code be incorporated in the standard library?  Should we start
    converting the standard library docs to reStructuredText?

`Timothy Delaney on comp.lang.python, 2002-04-03`__:

__ http://mail.python.org/pipermail/python-list/2002-April/096013.html

    I read through all the reStructuredText docs, comparing the text
    versions to the html versions.  I found the text versions to be
    *very* easy to read, whilst making it obvious in most cases when
    something was "special".

    I particularly like the system of doing hyperlinks...

    Definitely +1 from me ... I would really like a standard, clean
    docstring format.  Might make it easier to get my next project
    done in Python...

`Guido van Rossum on Python-Dev, 2002-04-03`__:

__ http://mail.python.org/pipermail/python-dev/2002-April/022212.html

    I think that reStructuredText is a good format for marking up
    docstrings; it's probably as good as it gets given the
    requirements (a fairly elaborate feature set, yet more readable
    "in the raw" than HTML).

`Richard Jones on comp.lang.python, 2002-04-03`__:

__ http://mail.python.org/pipermail/python-list/2002-April/096117.html

    How I see it is that ReST is a middle ground between markup and
    non-.  It has markup, and you can use it to the extreme.  Or you
    can follow some simple conventions (the most basic form of markup)
    and not worry about all the finer detail stuff. The difference
    between::

        @section{The Section Title}

    and::

        The Section Title
        -----------------

    Is pretty clearly to me that the second doesn't *look* like
    markup, even though it is.

`Guido van Rossum on Python-Dev, 2002-04-04`__:

__ http://mail.python.org/pipermail/python-dev/2002-April/022247.html

    Structured text is really a great idea for certain situations;
    reST is a much better implementation of the idea than any versions
    I've seen before.

`Max M on comp.lang.python, 2002-04-05`__:

__ http://mail.python.org/pipermail/python-list/2002-April/096656.html

    Any programmer can learn the basics in 15 minutes or less.

    And it really is very very easy to write documents in it.  I do
    belive that if I were ever to write a book (again) I would write
    it in ReST.

    And as far as I can tell from the specs, ReST solves most of the
    problems I have had with structured text.  A few things gets a
    little more complicated and some get simpler.  All in all a good
    bargain.

    I would certainly use it.  I also hope that it gets integrated
    into Zope.

`David Abrahams on Python-Dev, 2002-04-06`__:

__ http://mail.python.org/pipermail/python-dev/2002-April/022443.html

    Incidentally, I'm really excited about reST.  I've been looking
    for a tolerable markup for C++ comments, and reST looks like it
    might fit the bill.

`Eric Jones on Python-Dev, 2002-08-01`__:

__ http://mail.python.org/pipermail/python-dev/2002-August/027198.html

    I would very much like to see reStructuredText, or some minor
    variation on it, move forward as a "standard" for doc-strings very
    soon.  I have long lamented not having a prescribed format *and*
    an associated processing tool suite included in the standard
    library.  Even if the format isn't perfect (I think it looks very
    good), it is time to pick a reasonable candidate and go.

This being the Internet, there were plenty of people opposed to the
idea of reStructuredText, some vehemently.  Discovering *those* gems
is left as an exercise for the reader.

.. _Docutils: index.html
.. _StructuredText:
   http://dev.zope.org/Members/jim/StructuredTextWiki/FrontPage/
.. _Setext: mirror/setext.html
.. _statemachine.py: docutils/statemachine.py

.. |reStructuredText| image:: rst.png


..
   Local Variables:
   mode: indented-text
   indent-tabs-mode: nil
   sentence-end-double-space: t
   fill-column: 70
   End:
