# LINKGenerateReport

## Description
LINKGenerateReport examines all the documents in a database and produces a report.

## Syntax
```
status = LINKGenerateReport( <SourcePath>, <OutputPath>, <OutputTitle>, <Select>, <Flags> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| SourcePath | Input | String | The path to the databases to be processed. Separate the server and pathname with !! |
| OutputPath | Input | String | The path to the Validator report database. Validator will create this database if it doesn't exist. Separate the server and pathname with !! |
| OutputTitle | Input | String | The title to use if the report database needs to be created. |
| Select | Input | String | Used to specify the selection formula or view when searching data documents. If you only specify the LINK_VERIFY_DOCUMENTS flag, this parameter should contain a selection formula to select the documents to be processed. If you also specify the LINK_VERIFY_DOCUMENTS_BYVIEW flag, this parameter should be the name of the view that selects the documents. |
| Flags | Input | Long | A combination of the LINK_xxx values below. |

## Flags
| Flag | Description |
| --- | --- |
| LINK_VERIFY_DOCUMENTS | Have Validator run on documents. |
| LINK_VERIFY_DESIGN | Have Validator run on design notes. |
| LINK_VERIFY_DOCUMENTS_BYVIEW | When specified with LINK_VERIFY_DOCUMENTS, run on documents selected by a view rather than a selection formula. |
| LINK_FLAG_REPORT_ALL | Report all links, including good ones. |
| LINK_FLAG_NO_WARNINGS | Do not report warnings. |
| LINK_FLAG_NO_URLS | Do not check URLs. |
| LINK_FLAG_NO_EXTERNAL_LINKS | Do not allow links that point to a database other than the current one. |
| LINK_FLAG_NO_REPL_LOCAL | Do not search replicas that are not local. |
| LINK_FLAG_NO_FIELDS | Do not check fields. |
| LINK_FLAG_NO_EMPTY_FIELDS | Ignore empty fields. |
| LINK_FLAGS_DEFAULT | Use Validator defaults (no UI, run on documents). |
| LINK_RUN_SILENT | Hide the UI. |
| LINK_IGNORE_CONFLICTS | Do not check for save or replication conflicts. |

## Return Value
| Return value | Type | Description |
| --- | --- | --- |
| status | Long | Zero (0) indicates that no error occurred. If the return value is non-zero, use [LINKStringLoad](scriptstringload.md) to get the error message associated with the error code. |

## Examples
``` vbscript
status = LINKGenerateReport(
    "myserver!!dbToRun.nsf",_
    "linkreport.nsf",_ 'Database for output report
    "Validator Report",_ 'Title to use if linkreport.nsf needs to be created
    "@ALL",_ 'Selection formula for documents
    LINK_FLAGS_DEFAULT)
```