# Configuring CIAO! to Watch Documents

You can watch documents using CIAO!. You configure watching documents on a per-database basis. Examples of documents you may want to watch include those with configuration information or website content. Typically, you don't watch documents for production applications.

## To enable document watching
1. Open the CIAO! Config database and find the entry for the database you want.
2. Open the configuration database entry for the database.
3. Click the **Watch** tab.
4. Set the **Watch Documents** option to **Yes**.  
   CIAO! will then watch any document that contains the $TMSTitle field. This field is of type Text, and contains the text you want to use to reference this document. These documents appear in the CIAO! user interface as type Document, with the title set to the value of $TMSTitle.  
   You can then check Documents in and out as usual.
   
!!! note
    To stop watching a document, check it out and remove its $TMSTitle field.
    
In the following example, the $TMSTitle field was added to a single document in the database, and the value *This is a document* was entered into that field:
<figure markdown="1">
  ![Watched Document](img/admindocuments.png)
</figure>
 