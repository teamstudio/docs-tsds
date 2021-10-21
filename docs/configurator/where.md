# Specifying Where to Search

If you select the **Design** check box, Configurator can search for occurrences of the search text anywhere in the database design. This includes all of the formula code, LotusScript, static text on forms, subforms, help\using and help\about documents, field help, popups, element titles (for example, form titles and view titles)—in fact just about anywhere you can change text.

If you select the **Recompile modified design notes** check box, then when Configurator changes formula and LotusScript code, it checks the syntax and then recompiles the code. So if you make a change that causes a syntax error, you must fix the code before you can save the element.

If a change in source code causes an error, Configurator records that in its log. When you click **Replace All**, and your change causes an error, the original source code does not change. When you click **Replace**, and your change causes an error, Configurator gives you the option of saving the original source code or saving the source code with the error-causing changes. If you save an element with syntax errors, Configurator will not save the compiled (object) code for that element.  Configurator only saves the object code from an error-free compile.

You use the **Documents** option to search and replace strings in any fields that contain text.

!!! note
    Configurator only changes text found in the field—not the actual field name.
 
Within the following items, Configurator can Search but cannot Replace:
* Composite Apps
* Wiring properties
* Components
* Outlines
* ACLs

You can specify which documents to include in a search by specifying a selection formula (like a selection formula in a view), or by selecting an existing view.

## Specifying Your Selection by Formula or View
You can select documents by formula or by view.

### To select documents by formula
From the Teamstudio Configurator tab, click the Select by: Formula option button.

When you select documents by formula, the default is the formula **@ALL**, which means all documents in the database. For example, you can select all documents that were created with the MainTopic form by specifying the formula:
```
Form = "MainTopic"
```

### To select documents by view
From the Teamstudio Configurator tab, click the Select by: view option button. 

You see a box containing a list of views in the database design.
Select the view you want.
<figure markdown="1">
  ![Select View](img/where.png)
</figure> 
