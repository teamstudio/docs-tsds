# Specifying Where to Store Results

When Configurator finishes an action, it displays an on-screen log of the results. If you prefer, you can store the logs in a Notes database as a historical record of the changes you made using Configurator. 

## To store Configurator results in an output database
1. From the **Output** tab, select **Output log to database**.
2. Optionally select **Use a separate response document for each design element**, so that you can view a document for each element's results, rather than a single longer document for all results.  
   ![Output](img/results.png) 
3. In the **Report Document Title** box, enter a title for the report.
4. Click **Select** to locate a database in which to store the report.  
   You see only databases based on the reports template. The reports template name is **TMSLogs**, and the file name is **tmslogs.ntf**.  
   Select an existing database or specify a new database server/pathname.

Configurator bases the new database on the TMSLogs template and creates the output database for you. You can store Configurator report documents for more than one database in the same output database.

!!! note
    Each time you run Configurator, whether on the same database or different databases, change the report title. This makes it easier to locate log reports in the output database. 