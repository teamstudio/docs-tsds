# Report Options

The following report options are available:

| Option | Description |
| --- | --- |
| Smart Filter | Select **Smart Filter** to hide or filter information that is of no practical interest when comparing the database designs.</br>For example, an Agent stores information about the last time it was run. This is likely to be different between two different copies of a database, but does not really mean that there are differences in the design. With **Smart Filter** selected, Delta ignores that attribute. |
| Hide identical objects | Select the **Hide identical objects** check box to include in the report only elements or documents that are different. Clear this check box to include in your report the complete database design--elements and documents that are identical and elements and documents that are different. |
| Hide properties | Select the **Hide properties** check box to list the name only of design elements or documents that are different. Details about the differences are not included in the report, so you cannot learn what or where the differences are. This option produces a significantly shorter report. |
| Hide identical properties | Select the **Hide identical properties** check box to exclude from the report any identical individual properties for an object with differences. This means that objects with differences are included in the report, but within those differences any identical properties are excluded. This option produces a shorter document for each design element or document comparison. |
| Hide unique Notes | Select the **Hide unique Notes** check box to exclude from the report any Notes that exist in only one of the databases you are comparing. |