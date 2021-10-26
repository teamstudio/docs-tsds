# CIAOCreateCheckoutReport

## Description
Generates a report of checkouts for each design element in the database you specify using a description title for the report.

## Syntax
```
status = CIAOCreateCheckoutReport( <SourcePath>, <OutputPath>, <OutputTitle>, <Description> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| SourcePath | Input | String | The path to the Notes database that you want to process. Separate server and pathname with !! This database must be under CIAO! control and have the correct log specified in the CIAO! configuration. |
| OutputPath | Input | String | The path to the Notes database where you want CIAO! to write the report. Separate server and pathname with !! If this database does not exist, CIAO! will create it. |
| OutputTitle | Input | String | The title to use if the output database needs to be created. |
| Description | Input | String | The title for the report. |

## Return Value
| Return Value | Type | Description |
| --- | --- | --- |
| status | Long | Zero (0) indicates that no error occurred. If the return value is non-zero, use CIAOStringLoad to get the error message associated with the error code. |

## Example
```vbscript
Dim status As Long
Dim strPath As String
strPath = ""
If strDatabaseServer <> "" Then
    strPath = strDatabaseServer + "!!"
End If
strPath = strPath + strDatabasePath
status = CIAOCreateCheckoutReport( strPath, "CIAO\\Reports.nsf", "CIAO Checkout Report", "Sample Title" )
If status <> 0 Then
    Dim szBuffer As String*255
    CIAOStringLoad status, szBuffer, 255
    MessageBox Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 )
End If
```