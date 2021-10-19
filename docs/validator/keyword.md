# Keyword Field Contains Incorrect Values

Values that are currently stored in this keyword field do not agree with the values that would be presented to the user. One reason for this is a design change that caused keyword values to change.
 
The following is an example: 
<figure markdown="1">
  ![Error](img/keyword.png)
</figure>

In addition to the information common to all reports, the **Keyword Field Contains Incorrect Values** report shows the following:

| Field | Description |
| --- | --- |
| Design Name | The name of the form that Validator used with this document. |
| Field Name | The name of the failing field. |
| Unknown Value | List of values that were found in the field but were not valid choices according to the design. |
| Allowed Value | List of values that the user can choose from. |
