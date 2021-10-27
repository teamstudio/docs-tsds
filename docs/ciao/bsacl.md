# ACL and ACL Entries

## Setting the ACL
Use Teamstudio CIAO! to set the ACL of the file being promoted.  
**Note**: The ACL will be set for the file (normally a template) that is being promoted; the ACL of any database which is linked to this template will not be affected.

### To set your database or template ACL:
1. Select the Build or Promotion Path that relates to the database or template, for which you want to set a specific ACL.
2. Click the **Create** action button and select ACL. The ACL document appears:  
   ![ACL Document](img/bsacl.png)
3. The ACL document is active by default. Leave this setting.
4. Enter a descriptive name in the Description field (for example, Set Production ACL).
5. Select a **stored** ACL or define your own. For a stored ACL:
    1. Select the Store ACL option.
    2. Select a stored ACL from the list
    3. Click OK.
6. For a **defined** ACL:
    1. Select the Define ACL here option.
    2. In the Roles field, enter the roles you want to use for this database.  Enter one role per line.
    3. These roles appear when you add new ACL Entry documents to your database, within CIAO!.
    4. In the Administration Server field, enter the name of the target database’s administration server.
    5. Enter an Administration Server Flag or select one from the list.
    6. Select Enforce a consistent ACL across all replicas to ensure consistent ACLs across replicas.
    7. Select the Maximum Internet name and password from the list.

Save and close the document.

**Note**: If you do not define an ACL step for a promotion, the ACL of the source template will be copied to the promoted template unchanged.

**Note**: It is normally a requirement that the ID being used to perform the promotion be given Manager rights to the database being promoted, otherwise when the database is promoted a second time, the promoting ID will not have rights to overwrite it.

The new ACL entry appears in the right pane, under the Build or Promotion Path to which it applies.
<figure markdown="1">
  ![ACL Step](img/bsacl2.png)
</figure>
 
## Adding ACL Entries
Use Teamstudio CIAO! to add ACL entries to your database.

### To add ACL entries: 
1. Select the ACL document under the Build or Promotion Path that relates to the database or template, for which you want to add ACL Entries.
2. Click the **Create** action button and select ACL Entry. The ACL Entry document appears:  
   ![ACL Entry Document](img/bsacl3.png)
3. The ACL document is active by default. Leave this setting.
4. Use the dropdown beside the Name field to select a name from one or more address books. To set the default user ACL, use the text “-Default-” as the name.
5. Use the dropdown beside the Type field to select the ACL type specific to this entry.
6. Use the dropdown beside the Level field to select the ACL level specific to this entry.  
   **Note**: When you select a level, additional checkboxes appear, letting you specify optional and default access rights (for example, to replicate or copy documents, or to create documents)
7. Select the roles that are specific to this entry.

Save and close the document.

The new ACL entry appears in the right pane, under the ACL to which it applies.
<figure markdown="1">
  ![ACL Entry Step](img/bsacl4.png)
</figure>

**Note**: If you create an ACL Entry action, CIAO! requires that you have a least one manager defined in the ACL entries before you can promote.
