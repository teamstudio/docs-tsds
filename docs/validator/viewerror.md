# Viewing an Error

To view a Validator error, select a report document.
<figure markdown="1">
  ![Viewing an Error](img/viewerror.png)
</figure>

The Validator report shows the following:

* The options you have selected
* Database information
* Information about the error
* Information about where the error was found

Use this information to correct your database design.

## Common Information
The following information is common to all Validator reports.

| Field | Description |
| --- | --- |
| Time Run | The time Validator generated the report. |
| Options | The options you set when you ran the report (for example, include valid links in report and ignore empty fields). |
| Title | The name of the database you searched. |
| Server | The server location of the database you searched. |
| Database | The database against which the report was run. |
| NoteID | The failing element ID. |
| UNID | The 16-byte value that is assigned to a note when the note is first created. This value uniquely identifies a note. |
| Note | The name of the element. |
| Doclink | A doclink to the failing document. |
| Test Name | The type of test run. This is internally defined, consequently you cannot customize it. |
| Result | The result of the test (for example, Database was not found). |
| Error # | The error number (for example, 259). This is internally defined, consequently you cannot customize it. |
| Message | Information about the potential causes of the error. |
