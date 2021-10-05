# TMSSearchAll

This function is the same as **TMSRTContains** except it looks in all text and rich text fields on a document.

## Parameters
| Parameter | Meaning |
| --- | --- |
| **Flag** | This number tells TMSSearchAll how to search. These flags can be OR'd together |
| **Value** | This is the text to search for. It can be a quoted string or an unquoted field name. If it is a field name, Auditor gets the value to search for from that field, so it must be plain text. |

## Flags

| Flag | Flag Meaning |
| --- | --- |
| 0 | Normal |
| 1 | Whole Word |
| 2 | Case Sensitive |
| 4 | Accent Sensitive |
| 8 | Wildcards |
