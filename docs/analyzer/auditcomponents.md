# Auditor Components

Auditor uses several databases to identify the design elements you want to find, as described in the following table:

| Database | Description |
| --- | --- |
| Filters (based on deanfltr.ntf) | Describes the criteria to use when auditing a design. |
| Analysis (for example, analysis.nsf) | Created by Analyzer when a design is analyzed. |
| Audit output (for example, auditreport.nsf) | Documents the instances of design elements selected by Auditor which match filters. |

When Auditor runs, it retrieves the filter(s) from the Filters database and scans the analysis file looking for design elements that match those filter(s). For each match, Auditor creates a document in the audit output database.