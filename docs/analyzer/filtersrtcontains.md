# TMSRTContains

This function searches the specified rich text field for a value.
```
TMSRTContains( FieldName ; Flags; Value )
```

## Parameters
| Parameter | Meaning |
| --- | --- |
| **FieldName** | <p>This parameter represents the name of a rich text field on the current analyzer document.</p><p>If **Apply To** is **Agent**, then it includes only rich text fields that exist on the **Agent** form in the analyzer template.</p><p>Or</p><p>If this parameter is set to Rich Text, then it looks in all rich text fields on the document.</p>
| **Flag** | This number tells TMSRTContains how to search. These flags can be OR'd together |
| **Value** | This is the text to search for. It can be a quoted string or an unquoted field name. If it is a field name, Auditor gets the value to search for from that field, so it must be plain text. |

## Flags

| Flag | Flag Meaning |
| --- | --- |
| 0 | Normal |
| 1 | Whole Word |
| 2 | Case Sensitive |
| 4 | Accent Sensitive |
| 8 | Wildcards |
