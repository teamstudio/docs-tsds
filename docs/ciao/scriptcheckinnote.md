# CIAODbCheckIn/OutNote2

## Description
Check in or check out a document.

## Syntax
### CIAODbCheckOutNote2
```
status = CIAODbCheckOutNote2( <DatabaseHandle>, <NoteID>, <Comment>, <Flags> )
```

### CIAODbCheckInNote2
```
status = CIAODbCheckInNote2( <DatabaseHandle>, <NoteID>, <Comment>, <Flags> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| DatabaseHandle | Input | Long | A handle to a notes database opened using a LotusScript-wrapped  call to NSFDbOpen. |
| NoteID | Input | Long	| The id of the note to process. If you have a string value returned from the NoteID property, you can convert it to a number using code like `noteID = Val("&H" & doc.NoteID & "&")` |
| Comment | Input | String | The comment to use for the operation. |
| Flags | Input | Long | Flags to control the operation. You can pass 0 or a combination of the flags specified below. Multiple flags may be combined using the plus sign (+). |

## Flags
| Flag  | Description |
| --- | --- |
| CIAO_COMMENT_PROMPT | Display a dialog allowing the user to modify the comment. This option is rarely used for API operations that provide their own comment. |

## Return Value
| Return Value | Type | Description |
| --- | --- | --- |
| status | Long | Zero (0) indicates that no error occurred. If the return value is non-zero, use CIAOStringLoad to get the error message associated with the error code. |

## Example
```vbscript
Declare Function NSFDbOpen Lib "nnotes.dll" (Byval PathName As String, rethDB As Long) As Integer
Declare Function NSFDbClose Lib "nnotes.dll" (Byval hDB As Long) As Integer
  
hexNoteId = InputBox("Enter Note ID of design element to check out, as HEX", "NOTEID")
comment = InputBox("Enter a comment", "COMMENT")
flags = 0 'Flags can be set to CIAO_COMMENT_PROMPT, we have already prompted so no flags.
     
noteId = Val("&H" & hexNoteId & "&")
  
status = NSFDbOpen(db.server + "!!" + db.filePath, hdb)
If 0 <> status Then
    Error status
End If
  
status = CIAODbCheckOutNote2(hdb, noteId, comment, flags)
  
NSFDbClose(hdb)
```