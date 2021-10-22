# DIFFReportW32

## Description
DIFFReportW32 and DIFFDataReportW32 compare the design or data of two databases and write the results to a log.

## Syntax
### DIFFReportW32
```
status = DIFFReportW32( <Left>, <Right>, <Report>, <Title>, <Template>, <Filter>, <Flags> )
```

### DIFFDataReportW32
```
status = DIFFDataReportW32( <Left>, <Right>, <Report>, <Title>, <View>, <Template>, <Filter>, <Flags> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| Left | Input | String | The path to the first of the databases to be compared. Separate the server and pathname with !! |
| Right | Input | String | The path to the second of the database to be compared. Separate the server and pathname with !! |
| Report | Input | String | The path to the Notes database where the comparison report will be written. Separate the server and pathname with !! |
| Title | Input | String | The title to use if the report database needs to be created. |
| View | Input | String | **DIFFDataReportW32 only**. The name of the view to be used to find and sort the documents to be compared. This view must be present in both databases. |
| Template | Input | String | The path to the template to use if the report database needs to be created. If you provide an empty string ("") then the default template, **tmslogs.ntf** will be used. |
| Filter | Input | String | Reserved for future use. Must be "". |
| Flags | Input | Long | A combination of the DBDIFF_FLAG_xxx values below. |

## Flags
| Flag | Description |
| --- | --- |
| DBDIFF_FLAG_SILENT | Prevents UI feedback. |
| DBDIFF_FLAG_SINGLE | Produces one large report document rather than using response documents. Only suitable for comparing small databases. |
| DBDIFF_FLAG_SMART_FILTER | Use the Delta Smart Filter. |
| DBDIFF_FLAG_HIDE_ID_OBJECT | Hides identical objects. |
| DBDIFF_FLAG_HIDE_PROP | Hides properties. |
| DBDIFF_FLAG_HIDE_ID_PROP | Hides identical properties. |
| DBDIFF_FLAG_DEFAULT | Default options. Includes all of the other options except for DBDIFF_FLAG_HIDE_PROP. |

## Return Value
| Return value | Type | Description |
| --- | --- | --- |
| status | Long | Zero (0) indicates that no error occurred. If the return value is non-zero, use [DIFFStringLoadW32](scriptstringload.md) to get the error message associated with the error code. |

## Examples
### DIFFReportW32
```vbscript
status = DIFFReportW32(
    "db1.nsf",_
    "db2.nsf",_
    "report.nsf",_ 'Database for output report
    "Delta Report",_ 'Title to use if report.nsf needs to be created
    "",_ 'Use the default tmslogs.ntf template if report.nsf needs to be created
    "",_ 'Not used, must be empty
    DBDIFF_FLAG_SILENT + DBDIFF_FLAG_SMART_FILTER)
```

### DIFFDataReportW32
```vbscript
status = DIFFDataReportW32(
    "db1.nsf",_
    "db2.nsf",_
    "report.nsf",_ 'Database for output report
    "Delta Report",_ 'Title to use if report.nsf needs to be created
    "vwSelect",_ 'Name of view to select and sort documents to be compared
    "",_ 'Use the default tmslogs.ntf template if report.nsf needs to be created
    "",_ 'Not used, must be empty
    DBDIFF_FLAG_SILENT + DBDIFF_FLAG_SMART_FILTER)
```