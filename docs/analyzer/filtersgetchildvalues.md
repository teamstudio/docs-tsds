# TMSGetChildValues

This function returns a colon-separated list of field values from child documents in the Analyzer database.

## Parameters
| Parameter | Meaning |
| --- | --- |
| **&lt;Form Alias&gt;** | <p>This parameter indicates a form that can be a child of the current document.</p><p>For example a **column** can be a child of a **view**, but a **field** cannot.</p> |
| **&lt;field name&gt;** | <p>This parameter represents a valid text field on the child documents, for example, `TMSGetChildValues(CCOL00::fcolTitle)`.</p><p>When run against a view, the document returns a list of titles for all of the child columns.</p> |
