# Script Overview

You can start Analyzer using LotusScript. Use the Analyzer script library, located in the Teamstudio Reports template (tmslogs.ntf), to set up an analysis to be run in batch.

This section provides detailed descriptions of each Analyzer script library function, followed by agent examples that illustrate how to use it.

The Analyzer Script Library exposes the following functions:

| Function | Description |
| --- | --- |
| [DEANAnalyzeW32](scriptanalyze.md) | Calls Analyzer. Passes only the file names and flags. |
| [DEANAnalyze2W32](scriptanalyze2.md) | Calls Analyzer. Passes the file names, output database title, the template to be used when creating the output database file, flags and a filter indicating the types of design elements to be analyzed. |
| [DEANAnalyzeAndAudit](scriptanalyzeandaudit.md) | Calls Analyzer Audit. Performs an analysis and audit on a given database. |
| [DEANStringLoadW32](scriptstringload.md) | Obtains the error message associated with any error code returned from the other API functions. |

If you work within the Teamstudio Reports template (tmslogs.ntf), you will not have to worry about creating the Analyzer script library. If you work within a different database/template, you must copy over this script library as well.