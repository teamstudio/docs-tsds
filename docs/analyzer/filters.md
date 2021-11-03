# Overview

Filters identify design objects you want to focus on. You define filters by specifying the attributes and properties that meet your criteria.

## Analyzer Filter Examples
* Use of @dblookup in a keyword definition (potential performance problem)
* Editable text fields without Help text (violations of organizational standards)
* Non-computed fields ending in "_1" (common coding errors)
* Existence of a certain design element (for example, Help Using, Help About or a particular form)
* Use of specific field properties (for example, Date/Time fields that don't display the year with four digits)

Auditor scans the analysis output looking for design objects that match the filter criteria and documents each occurrence in the audit output database. 

Since most development organizations have their own standards and procedures, you may want to add your own filters, modify the severity to match terms and criteria you use, and classify filters with terms you normally use. With Auditor, it's easy to customize filters and their attributes to meet your organization's needs. 

You can find the filters and definitions of their attributes (class and severity) in the Analyzer Filter database. The Analyzer Filters database included in this release is **deanfltr.ntf**. Prior to Edition 24, it was **deanfltr.nsf**. This is so the install database does not overwrite the filter database currently on your system. If you have modified the database in any way, you will not lose any changes or customization. However, this means that you must create a new filter database if you want to incorporate the bug fixes included with this release. 

## To upgrade your filters database
1. Make a copy of your current Analyzer Filters Database (**deanfltr.nsf**)
2. Create a new database (**File > Database > New**) and name it **deanfltr.nsf**
3. Select Analyzer Filters Template from the template box.
4. Click **Yes** when Notes asks if you want to overwrite the existing one. (It's OK; you made a copy)
5. Copy all your custom filters into this new database from your old one.

The attribute, Class, groups the same type of filters together. For example, filters that identify design techniques that can cause problems when you upgrade to a new Notes Release are typically categorized as Release "A" to Release "B" Upgrade Issues. Therefore, you can set up a class called Release A to Release B Upgrade or simply, Upgrade. Then, when you define a filter that fits this category, you assign it to the Upgrade class. At run-time, you tell Auditor which class of filters to use. 

The Severity attribute prioritizes the documents stored in the audit output database, helping you to systematically review and act on the items selected. 
