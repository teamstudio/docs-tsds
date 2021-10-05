# TMSIncludeChildren

This function runs the specified filter against all children of the current document and combines the results according to the specified logic.

## Parameters
| Parameter | Meaning |
| --- | --- |
| **UNID** | This parameter is the UNID of the filter document you will use to run against the child documents. |
| **LOGIC** | <p>Accepts values "AND" and "OR".</p><p>"AND" - result will be true only if the filter evaluates to true for all children. "OR" - result will be true if the filter evaluates true for at least one child.</p> |

Use the **Select filter(s) to evaluate against children** button on the **filter definition** form to set up TMSIncludeChildren.

For example:
```vscript
TMSIncludeChildren(" FA385C79559C18308525690B006479B6";"AND")
```
