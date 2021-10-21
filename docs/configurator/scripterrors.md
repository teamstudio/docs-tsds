# Configurator Error Code Return Values

These are possible return values for any of the Analyzer functions.

| Value | Meaning |
| --- | --- |
| NOERROR (0) | Operation completed successfully. |
| 0-65535 | Notes API error codes. |
| 65536 and above | Teamstudio error codes |

| Teamstudio Error Code Value | Meaning |
| --- | --- |
| IDERR_STAR_BAD_SELECTION_FORMULA (67585) | The selection formula specified is invalid. |
| IDERR_STAR_BAD_SOURCE_DB (67586) | The source database path is invalid. |
| IDERR_STAR_BAD_FIND_STRING (67587) | The find string is invalid (e.g. not a valid regular expression.) |

!!! note
    Many other possible error codes can be returned. Use [CONFYStringLoad](scriptstringload.md) to get the message associated with an error code.