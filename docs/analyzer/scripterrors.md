# Error Code Return Values

These are possible return values for any of the Analyzer functions.

| Value | Meaning |
| --- | --- |
| NOERROR (0) | Operation completed successfully. |
| 0-65535 | Notes API error codes. |
| 65536 and above	| Teamstudio error codes |

| Teamstudio Error Code Value	| Meaning |
| --- | --- |
| IDERR_DEAN_BAD_CLASS (66816) | The design class of the pre-existing analysis database is not DEANTemplate |
| IDERR_DEAN_BAD_ANALYSIS (66817) | The pre-existing analysis database contains invalid documents. |
| IDERR_DEAN_DELETE_FAILED (66820) | Analyzer could not remove analysis documents corresponding to deleted design elements. |
| IDERR_DEAN_TEMPLATE_NOT_FOUND (66821) | Analysis template (usually **ivesdean.ntf**) could not be found. |

!!! note
    Many other possible error codes can be returned. Use [DEANStringLoadW32](scriptstringload.md) to get the message associated with an error code.