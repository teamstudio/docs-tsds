# DEANAnalyzeW32

## Description
Calls Analyzer. Passes only the file names and flags.

## Syntax
```
status = DEANAnalyzeW32( <Design>, <Analysis>, <Flags> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
|Design | Input | String | The path of the database to analyze. Separate server and pathname with !!
| Analysis | Input | String | The path of the analysis output database. Separate server and pathname with !! |
| Flags | Input | Long | This parameter allows you to control how Analyzer runs. You can pass any of the [DBDEAN Flag Constants](scriptflags.md). You can pass a combination of flags by using a plus sign (+) to combine them. |

## Return Value
| Return Value | Type | Description |
| --- | --- | --- |
| status | Integer | A return value of zero (0) indicates that no error has occurred. If the return value is non-zero, use [DEANStringLoadW32](scriptstringload.md) to retrieve the error message associated with the error code. |

## Example
``` vbscript
status = DEANAnalyzeW32(_
    "myserver!!dbtorun.nsf",_ 'database to analyze
    "dbout.nsf",_ 'analysis database for output
    DBDEAN_FLAG_SILENT + _ 'no UI feedback
    DBDEAN_FLAG_NO_CREATE) 'do not create new analysis database
```