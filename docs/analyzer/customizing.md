# Customizing the Template

When Analyzer is installed, it creates a database template file called **ivesdean.ntf**, which has a template name of DEANTemplate. Analyzer uses this template to create the analysis output database. The database stores the analysis documents for one or more Notes template or database designs.
 
!!! note
    LotusScript, formula code, Java and JavaScript are always written as rich text.  This is because plain text fields are limited to around 15K in size by the Notes client, and code can be as large as 64K. Since you cannot refer to rich text fields in view selection formula, this may at first seem limiting. You can create an agent which performs an @Abstract operation on the rich text, converting it to plain text, truncating it at some size less than 15K. For example:  
    ```
    FIELD ScriptBegins :=
    @If(fflpScripts="";"";@Abstract([Save]:[Abbrev];14999;"";"fflpScript"))
    ```
 
You can customize the template to create additional views or Notes agents.

## To create a template you can customize
1. From Notes, make a new copy of the Teamstudio Analyzer Template (**ivesdean.ntf**).
2. Open the Database Properties window for the new file. Then click the Design tab.
3. From the Design tab, rename the new template.
4. In the Database Categories box, enter **DEANTemplate**.

When creating a new output database, you base its design on a template that you select from a list of all the templates you have created.

You can add fields to the forms in the output database template. The fields can hold information, such as comments, that you add to the database. These additional fields are not overwritten when the analysis output is updated.

!!! note
    The content of user-defined fields is only preserved between Analyzer runs for design notes and fields.
    
Similarly, you can add forms to the output database template to hold any data you want to capture. You can create and edit these forms, optionally using formulas and scripts that extract data created by Analyzer into your form.

!!! note
    While a user-defined form is not overwritten when the analysis output is updated, the documents created with user-defined forms will only be preserved between Analyzer runs for main documents and responses to design notes and fields.