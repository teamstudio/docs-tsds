# DBDEAN Flag Constants

| Flag | Description |
| --- | --- |
| DBDEAN_FLAG_ACL_SINGLEDOC | Writes all ACL users and their properties in a single document. |
| BDEAN_FLAG_DEFAULT |Default behavior is to create an output database if it doesn't exist, update only the elements that are modified since the last run and prompt if an error occurs. |
| DBDEAN_FLAG_NO_ANALYSIS | (For DEANAnalyzeAndAudit only.) Run the audit on an existing analysis database without also running the analysis. |
| DBDEAN_FLAG_NO_CREATE | Prevents creation of a new analysis database. If the specified analysis database does not exist, the function returns an error. |
| DBDEAN_FLAG_REBUILD_ALL | Prevents incremental update. The entire analysis will be deleted and rebuilt, except for user response documents. |
| DBDEAN_FLAG_SILENT | Prevents UI feedback. No messages will be displayed. You must check the returned error code to ensure that the analysis was successful. |
