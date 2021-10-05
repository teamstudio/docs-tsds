# Viewing Analysis

With the many sorting categories Analyzer provides, you can view the design element information you need. So where do you begin? To get started, consider the recommended views and actions described in the following table.

| Goal | What to View | What to Do |
| --- | --- | --- |
| See where design elements are used | View design element references | <ol><li>Expand the corresponding design element category with the left navigator, and open the design element document. The references are listed at the end of the document.</li><li>Go to the Design Aids view category and select the Dependencies view. This shows all design elements with dependencies by design element category.</li></ol> |
| See Last Modified | View all design element last modified dates | The Design Aids category has several views to show the last modified dates |
| See Default Access | View the database access control list | In the Analysis category, there is a subcategory for ACL analysis |
| Check view columns for consistency | View columns in views | In the Objects by Name category, there is a view called Columns in views that shows several settings that can often be inconsistent. |
| See subroutines in need of refactoring | View the number of lines and parameters of agents | In the design category, under Code and then Script Libraries, is a view called Subs that lists the number of lines of code and the number of variables declared. The largest numbers are the most complex subroutines and could be refactored. |
| See everywhere a field is referenced | Use the Field XRef folder | Simply drag any field document (under Forms in Object by Name category) and drop it in the xRef folder. Then click the Add References button. Every design element that refers to that field will be included in the view. |
