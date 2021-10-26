# Enabling or Disabling CIAO!

To remove a database from CIAO! control, you can edit the document for the watched database in the CIAO! configuration database.

## To edit the document for the watched database
1. Open the CIAO! Config database (usually on the server).
2. In the **Go To** section, click one of the Promotion Path views, for example, **Databases by Path**.  
   ![View](img/adminenable.png)
   <div class="admonition">
     <p class="admonition-title">Note</p>
     <p>The green check mark in the above figure indicates that the database is under CIAO! control. If you remove this database from CIAO! control, the icon will change to a red X.</p>
   </div>
3. Select the document describing the database you want to remove from CIAO! control, and open it for editing.
4. Change the value of the **CIAO! Watch Active** field from **Yes** to **No** to mark the database as no longer under CIAO! control.  
   ![Config Document](img/adminenable2.png)
 
!!! note
    Once you remove the watched database from CIAO! control, check-in/check-out will no longer work for this database. Any developer can make changes to any design elements.  
    You are *not* removing the history of the database. This remains in the CIAO! log database. You can also access the history if you haven't deleted it from the log database.
