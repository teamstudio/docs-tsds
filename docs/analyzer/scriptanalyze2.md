# DEANAnalyze2W32

## Description
Calls Analyzer. Passes the file names, output database title, the template to be used when creating the output database, flags and a filter indicating the types of design elements to be analyzed.

## Syntax
```
status = DEANAnalyze2W32( <Design>, <Analysis>, <Title>, <Template>, <Filter>, <Flags> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
|Design | Input | String | The path of the database to analyze. Separate server and pathname with !!
| Analysis | Input | String | The path of the analysis output database. Separate server and pathname with !! |
|Title | Input | String | The title to be used if a new analysis database is created. |
| Template | Input | String | The path to the template to use if a new analysis database is created. Separate server and pathname with !!. Specify the empty string, "", to use the default template. |
| Filter | Input | String | A [Context Filter](scriptctxfilter.md) string specifying which design elements should be analyzed. Specify the empty string, "", to analyze the full design. |
| Flags | Input | Long | This parameter allows you to control how Analyzer runs. You can pass any of the [DBDEAN Flag Constants](scriptflags.md). You can pass a combination of flags by using a plus sign (+) to combine them. |

## Return Value
| Return Value | Type | Description |
| --- | --- | --- |
| status | Integer | A return value of zero (0) indicates that no error has occurred. If the return value is non-zero, use [DEANStringLoadW32](scriptstringload.md) to retrieve the error message associated with the error code. |

## Example
``` vbscript
status = DEANAnalyze2W32(_
    "myserver!!dbtorun.nsf",_ 'database to analyze
    "dbout.nsf",_ 'analysis database for output
    "Analysis of dbtorun",_ 'title for output database
    "",_ 'use default template,
    "-*",_ 'analyze database level properties only
    DBDEAN_FLAG_DEFAULT) 'create analysis database if it doesn't exist
```