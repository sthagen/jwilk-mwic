====
mwic
====

---------------------------
Misspelled Words In Context
---------------------------

:manual section: 1
:version: mwic 0.1.2
:date: |date|

Synopsis
--------
**mwic** [-l *lang*] [*option*...] [*file*...]

Description
-----------
*mwic* is a spell-checking frontend that groups misspellings and shows them in their contexts.
This is useful for checking technical documents that often contain words that are not included in standard dictionaries.


Options
-------

-l lang, --language lang
   Spell-check for this language.
   The default is ``en``.

--list-languages
   Print list of available languages.

--input-encoding enc
   Assume this input encoding.
   The default is UTF-8.

--max-context-width n
   Limit context width to *n* characters.
   The default is 30.

--suggest n
   Suggest up to *n* corrections.

-h, --help
   Show the help message and exit.

--version
   Show the program's version number and exit.

Example
-------

::

   $ mwic debian-social-contract.txt
   DFSG:
   | …an Free Software Guidelines (DFSG)
   | …an Free Software Guidelines (DFSG) part of the
                                   ^^^^

   Perens:
   |    Bruce Perens later removed the Debian-spe…
   | by Bruce Perens, refined by the other Debian…
              ^^^^^^

   Ean, Schuessler:
   | community" was suggested by Ean Schuessler. This document was drafted
                                 ^^^ ^^^^^^^^^^

   GPL:
   | The "GPL", "BSD", and "Artistic" lice…
          ^^^

   contrib:
   | created "contrib" and "non-free" areas in our…
              ^^^^^^^

   CDs:
   | their CDs. Thus, although non-free wor…
           ^^^

.. |date| date:: %Y-%m-%d

.. vim:ts=3 sts=3 sw=3