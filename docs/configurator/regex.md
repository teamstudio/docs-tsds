# Using Regular Expressions

Configurator can search using the ECMAScript regular expression syntax. Describing regular expressions is beyond the scope of this documentation, and we recommend you do not use this option if you are not comfortable with them. Always test a regular expression using **Find** before performing a replacement, as it is easy to construct a regular expression that matches more text than you intended.

!!! note
    Configurator does not support capture groups in the replacement string. The **Replace with** value
    will be inserted verbatim when performing replacements.