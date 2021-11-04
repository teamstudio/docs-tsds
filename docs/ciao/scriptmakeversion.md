# CIAOMakeVersionImp

## Description
Creates a version of the database specified.

## Syntax
```
status = CIAOMakeVersion( <SourcePath>, <VersionLabel>, <Comment>, <VersionFlags>, <Flags> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| SourcePath | Input | String | The path to the Notes database that you want to process. Separate server and pathname with !! This database must be under CIAO! control and have the correct log specified in the CIAO! configuration. |
| VersionLabel | Input | String | The version label used in the Make Version process. This string cannot be blank. |
| Comment | Input | String | The version comment. This string can only be blank if Force Comments is not set in the CIAO! configuration. |
| VersionFlags | Input | Long | Flags to control the change in the version number of the new release. |
| Flags | Input | Long | Flags to control what is written to the report. |

## Version Flags
| Flag | Description |
| --- | --- |
| CIAO_MVERSION_NO_BUMP | Do not change the version number. |
| CIAO_MVERSION_BUMP_MAJOR | Increase the major version number, for example from 3.x.x to 4.0.0. |
| CIAO_MVERSION_BUMP_MINOR | Increase the minor version number, for example from 4.1.x to 4.2.0. |
| CIAO_MVERSION_BUMP_POINT | Increase the point version number, for example from 5.2.3 to 5.2.4. |

## Flags
| Flag | Description |
| --- | --- |
| CIAO_COMMENT_PROMPT | Prompt for a comment. |
| CIAO_MVERSION_SILENT | Do not display the status bar. |
| CIAO_MVERSION_PROMPT | Display the Make Version dialog box. |
| CIAO_MVERSION_DATA | Include documents in the version database. |
| CIAO_MVERSION_ACL | Include the ACL in the version database. |
| CIAO_MVERSION_REPID | Include the Replica ID in the version database. |
| CIAO_MVERSION_ODS_NOTES5 | Force the version database to have an R5.x ODS. |
| CIAO_MVERSION_ODS_NOTES4 | Force the version database to have an R4.x ODS. |
| CIAO_MVERSION_SAVE_ZIPPED | Save the version database as a zip file. |
| CIAO_MVERSION_DEFAULT | Does not display the status bar. Saves the version database as a zip file. |
| CIAO_MVERSION_UI_SHOW_STATUS | Updates the Notes status bar with the progress of the version operation. |
| CIAO_MVERSION_UI_SHOW_PROGRESS | Displays the progress bar. |
| CIAO_MVERSION_NO_UI | Does not display the UI. All options must be passed into the CIAOMakeVersionImp call. |
| CIAO_MVERSION_FULL_UI | Enable all options in the Make Version window. Without this, the version number fields are disabled. |

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
status = CIAOMakeVersionImp( strPath, "BASELINE", "Initial baseline version", CIAO_MVERSION_DEFAULT )
If status <> 0 Then
    Dim szBuffer As String*255
    CIAOStringLoad status, szBuffer, 255
    MessageBox Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 )
End If
```