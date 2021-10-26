# CIAOCreateChangeList

## Description
Generates a list of changes based on the database you specify and a range of version labels.

## Syntax
```
status = CIAOCreateChangeList( <SourcePath>, <OutputPath>, <OutputTitle>, <NewerVersion>, <OlderVersion>, <Flags> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| SourcePath | Input | String | The path to the Notes database that you want to process. Separate server and pathname with !! This database must be under CIAO! control and have the correct log specified in the CIAO! configuration. |
| OutputPath | Input | String | The path to the Notes database where you want CIAO! to write the report. Separate server and pathname with !! If this database does not exist, CIAO! will create it. |
| OutputTitle | Input | String | The title to use if the output database needs to be created. |
| NewerVersion | Input | String | Used to specify the end of the range of version labels that you want to include. Use an empty string ("") to include changes up to the current state of the database. |
| OlderVersion | Input | String | Used to specify the start of the range of version labels that you want to include. |
| Flags | Input | Long | Flags to control what is written to the report. You can pass 0 or a combination of the flags specified below. Multiple flags may be combined using the plus sign (+). |

## Flags
| Flag | Description |
| --- | --- |
| CIAO_REPORT_SILENT | Do not display the status bar. |
| CIAO_CL_REPORT_DELTA | Include differences in the report. |
| CIAO_CL_REPORT_OWNER | Include the person who checked in the element. |
| CIAO_CL_REPORT_DATE | Include the date the element was checked in. |
| CIAO_CL_REPORT_COMMENT | Include the checkin comment. |
| CIAO_CL_REPORT_IGNORE_NO_PREV | Ignore elements that do not have a previous checkin. |
| CIAO_CL_REPORT_DEFAULT | Doesn't display the status bar. Includes differences, the person who checked in the element, the checkin date and the checkin comment. |
 
## Return Value
| Return Value | Type | Description |
| --- | --- | --- |
| status | Long | Zero (0) indicates that no error occurred. If the return value is non-zero, use [CIAOStringLoad](scriptstringload.md) to get the error message associated with the error code. |

## Example
```vbscript
Dim status As Long
Dim strPath As String
strPath = ""
If strDatabaseServer <> "" Then
    strPath = strDatabaseServer + "!!"
End If
strPath = strPath + strDatabasePath
status = CIAOCreateChangeList( strPath, "CIAO\\Reports.nsf", "CIAO Change List", "", "BASELINE", CIAO_CL_REPORT_DEFAULT )
If status <> 0 Then
    Dim szBuffer As String*255
    CIAOStringLoad status, szBuffer, 255
    MessageBox Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 )
End If
```