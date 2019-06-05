.. role:: small

==============
RST Cheatsheet
==============

https://github.com/ralsina/rst-cheatsheet/blob/master/rst-cheatsheet.rst


Inline Markup
-------------

Inline markup allows words and phrases within text to have character styles (like italics and boldface) and functionality (like hyperlinks).

+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    *emphasis*                                            | *emphasis*                                     |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    **strong emphasis**                                   | **strong emphasis**                            |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       | The rendering and meaning of interpreted text  |
|                                                          | is domain- or application-dependent.           |
|    `interpreted text`                                    |                                                |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    ``inline literal``                                    | ``inline literal``                             |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    reference_                                            | reference_                                     |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    `phrase reference`_                                   | `phrase reference`_                            |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    anonymous__                                           | anonymous__                                    |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    _`inline internal target`                             | _`inline internal target`                      |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       | The result is substituted in from the          |
|                                                          | substitution definition.                       |
|    |substitution reference|                              |                                                |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    footnote reference [1]_                               | footnote reference [1]_                        |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    citation reference [CIT2002]_                         | citation reference [CIT2002]_                  |
+----------------------------------------------------------+------------------------------------------------+
| ::                                                       |                                                |
|                                                          |                                                |
|    http://docutils.sf.net/                               | http://docutils.sf.net/                        |
+----------------------------------------------------------+------------------------------------------------+

__ http://docutils.sourceforge.net/docs/user/rst/quickref.html#hyperlink-targets

.. _reference: http://docutils.sourceforge.net/docs/user/rst/quickref.html#hyperlink-targets

.. _phrase reference: http://docutils.sourceforge.net/docs/user/rst/quickref.html#hyperlink-targets
