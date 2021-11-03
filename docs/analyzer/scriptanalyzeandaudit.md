# DEANAnalyzeAndAudit

## Description
Calls Analyzer Audit. Performs an analysis and audit on a given database.

## Syntax
``` 
status = DEANAnalyzeAndAudit( <Design>, <Analysis>, <Title>, <Template>, <AuditIn>, <AuditOut>, <AuditOutTitle>, <AuditClass>, <Filter>, <Flags> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| Design | Input | String | The path of the database to analyze. Separate server and pathname with !! |
| Analysis | Input | String | The path of the analysis output database. Separate server and pathname with !! |
| Title | Input | String | The title to be used if a new analysis database is created. |
| Template | Input | String | The path to the template to use if a new analysis database is created.  Separate server and pathname with !!. Specify the empty string, "", to use the default template.
| AuditIn | Input | String | The path to the Auditor filter database. Separate server and pathname with !! |
| AuditOut | Input | String | The path to the Auditor output database. Separate server and pathname with !! | 
| AuditOutTitle | Input | String | The title to use if the Auditor output database needs to be created. |
| AuditClass | Input | String | The audit filter class to use for the audit. |
| Filter | Input | String | A [Context Filter](scriptctxfilter.md) string specifying which design elements should be analyzed. Specify the empty string, "", to analyze the full design. |
| Flags | Input | Long | This parameter allows you to control how Analyzer runs. You can pass any of the [DBDEAN Flag Constants](scriptflags.md). You can pass a combination of flags by using a plus sign (+) to combine them. |

## Return Value
| Return Value | Type | Description |
| --- | --- | --- |
| status | Integer | A return value of zero (0) indicates that no error has occurred. If the return value is non-zero, use [DEANStringLoadW32](scriptstringload.md) to retrieve the error message associated with the error code. |

## Example
``` vbscript
status = DEANAnalyzeAndAudit(_
    "myserver!!dbtorun.nsf",_ 'database to analyze
    "dbout.nsf",_ 'analysis database for output
    "Analysis of dbtorun",_ 'title for output database
    "",_ 'use default template,
    "deanfltr.nsf",_ 'default filter database
    "dbAuditOut.nsf",_ 'database for audit results
    "Audit of dbtorun",_ 'title for audit results database
    "UI Standards",_ 'filter class
    "-FM",_ 'analyze forms only
    DBDEAN_FLAG_DEFAULT) 'create analysis database if it doesn't exist
```