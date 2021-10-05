# TMSGetParentValue

This function gets a field value from a parent document in the Analyzer database.

```
TMSGetParentValue( <Form Alias>::<field name> )
```

## Parameters
| Parameter | Meaning |
| --- | --- |
| **&lt;Form Alias&gt;** | <p>This parameter must indicate a parent of the current document (following the structure of the Analyzer output).</p><p>For example, **field** cannot be a parent document of a **form**. However, **Form** can be a parent for a field. Also, the only valid parent for a design element is **Database** (CDBP00).</p> |
| **&lt;field name&gt;** | This parameter must represent a valid text field on the target document. Otherwise, it will fail. The field cannot be a rich text field. If the field is not a text field, the value is converted to text. |

For example, consider the following:
``` vbscript
TMSGetParentValue( CDBP00::fdbpFile )
```
It returns the file name of the current database. 

It can be embedded in the RT formula as follows:
```vbscript
TMSRTContains( Rich Text ; 0; TMSGetParentValue( CDBP00::fdbpFile ))
```
When checking a filter, **GetParentValue** is evaluated first and its return value is substituted into the formula. Then the rest of the formula is evaluated. This function works on any **ApplyTo** filter except **Database** because Database documents do not have a parent.