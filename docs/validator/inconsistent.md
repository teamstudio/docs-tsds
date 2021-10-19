# Fields Inconsistency

Fields stored on the document did not line up with fields on the design. Some potential causes for this include fields not needed that are deleted from the design leaving fields on the design that may not be used again and are just taking up space. Or the type of the field may have changed, for example, a text field that is now a number field.
 
The following is an example: 
<figure markdown="1">
  ![Error](img/inconsistent.png)
</figure>

In addition to the information common to all reports, the **Fields Inconsistency** report shows the following:

| Field | Description |
| --- | --- |
| Design Name | The name of the form that was used with this document. |
| Missing on design | Lists the fields that are in the documents but missing in the design, along with the field size of the documents in parentheses [field- name(size)]. |
| Missing on doc | Lists the fields that are in the design but not the documents. |
| Has different type | States differences between the field type in the design and the field type in the document. |
| Computed for Display (CFD) fields stored on document | This shows the number of CFD fields that Validator found stored on the document, along with the field size in parentheses [field-name(size)]. |