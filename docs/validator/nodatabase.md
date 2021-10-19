# Database was not Found

The database specified in the document link wasn't found. This means that the replica ID is no longer valid or the server that the database resides on is unavailable.

Reported errors can include the following:

* File does not exist
* File not found or not a Notes database
* You are not authorized to perform that operation

The following is an example:

<figure markdown="1">
  ![Error](img/nodatabase.png)
</figure>

In addition to the information common to all reports, the **Database was Not Found** report (unique for DocLink Reports) shows the following:

| Field | Description |
| --- | --- |
| Field | The field on the document where the link was found. |
| Type | The type of link (for example, DocLink or URL). |
| Format | How the link was stored (for example, standard, computed or special). |
| Element Name | Name of the element linked to by Named Element Link (only for the Type: Named Element). |
| NoteLink Type | Type of NoteLink (For example, Named Element, DocLink). |
| DBID | Database RepID. |
| View | View UNID. |
| Note | Note UNID. |
| Nearby Text | Text near the error, provided as a hint. |

!!! note
    A document link is composed of three parts: DBID, View and Note. Each must be valid for Notes to locate a doclink in the database. 