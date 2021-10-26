# CIAO! Log Fields

You can build custom views of the data. The CIAO! Log Database uses field names prefixed by the $ character. As such, the field names do not appear in the programmer's pane. The log database uses the following fields:
 
| | Field | Description |
| --- | --- | --- |
| | $CIAOProject | Name of the project, taken from the CIAO! configuration file. |
| * | $CIAODatabase | Name of the database, taken from the CIAO! configuration file. |
| | $CIAOType | Type of design element, (for example, Agent, Form or View). |
| | $CIAOName | Name of design element, for elements that support aliases this is the first name/alias. |
| | $CIAODisplayName | Name of design element, displayed as titled in the History view. |
| | $CIAOTime | Date and time the design element was checked in. |
| | $CIAOUser | Developer's name. |
| | $CIAOComment | Check-in Comment. |
| * | $CIAODBID | Unique code identifying each database (hidden). |
| | $CIAOUNID | Unique code identifying each design element (hidden). |
| * | $CIAOODSVersion | Notes release with which this database is compatible, as specified in the Version Options window. |
| * | $CIAOOriginalName | The original name of the database before it was renamed to version.nsf or version.zip during Make Version. |
| | $CIAO Revision | Version number of the element. |
| * | $CIAOVersionNum Pos 1/2/3 | Version number values, where 1/2/3 refer to major/minor/ point values. |

\* Only found in Database Version documents.
