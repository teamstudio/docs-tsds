# Sharing Design Changes through Merging

Delta's merge feature lets you quickly share design changes you choose between two databases. When you merge, you replace an object from one database with a copy of the object from another database. Note that merges in Delta happen in realtime.

Manual merging in Delta works on the object level. You can merge most objects from one database to another as long as the target database has the same "container" as the source. For example, a button in a form called Employees can be merged into another form called Employees in another database.

## To merge elements from two databases
You can merge elements from one database to another as follows:

1. With the source and target database displayed in Delta, right-click in one database on the element you want to merge to the other database.
2. Select **Merge this to Right** or **Merge this to Left** from the menu that appears.  
   ![Merge Menu](img/merging.png)  
   The element is merged into the other database. 
   
## Common Uses for Manual Merging
You can use manual merging in a variety of ways:

* Moving bug fixes or changes in an older version of an application to a newer version.
* After upgrading a third party application, merging modifications you have made to a previous version.
* Adding action buttons to forms.