# Overview

The simplest build path consists of a configuration document, describing the source template (or database), and a Promotion Path document, describing the target template location. On top of this CIAO! provides the ability to add any or all of the following optional steps:

* [Design Audit](bsaudit.md) – Calls Teamstudio Analyzer and checks the design of the source template against your coding and look and feel standards.
* [Make Version](bsversion.md) – Calls Teamstudio CIAO! and makes a controlled version of the design template.
* [ACL Settings](bsacl.md) – Sets the general ACL and specific ACL entries for the promoted template.
* [Database Properties](bsdbproperties.md) – Allows the title, categories, inherited from template name and master template name to be set, cleared or left alone. Also, version information such as the Template Version, Name and Date as well as the $TemplateBuild shared field can be edited.
* [Copy Database](bscopy.md) – Allows another copy of the source template to be made and placed in a different location.
* [Search and Replace](bssearch.md) – Calls Teamstudio Configurator allowing a search and replace to be done as part of the build. This is an excellent way to stamp user-visible elements of the design with the version number and the date of creation.
* [Compile LotusScript](bscompile.md) – Allows the compilation of all LotusScript or specific LotusScript elements within a promoted template as part of the build.
* [Element Properties](bselemproperties.md) – Allows the Prohibit Design Refresh flag, Propagate Prohibition flag, Design Element Inheritance option and Design Element Comment field to be edited.
* [Sign Database](bssign.md) – Allows the design (or database) a specific or stored ID as part of the build.
* [Refresh/Replace Design](bsrefresh.md) – Allows one or more target databases to have their designs refreshed or replaced with the promoted template.
* [Email Notification](bsemail.md) – Can be used to send email messages to individuals and/or groups at one or more points in a promotion.

These steps are a subset of the build steps available in Teamstudio Build Manager. Build Manager includes additional features to help manage complex build and release processes. For more information about Build Manager, see [Product Comparison - CIAO! and Build Manager](promotioncompare.md).