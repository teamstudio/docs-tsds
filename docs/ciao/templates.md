# Working with Templates

If a design element inherits its design from a template, CIAO! displays the template name in the owner column. CIAO! does not let you check those elements out. To change those elements, make changes in the source template.

To allow template-linked elements to be checked out, open the CIAO! Configuration database and set the **Watch Template Linked Elements** field to **Yes**.

* The default setting **No** indicates that CIAO! will not watch template-linked elements. In this case, CIAO! will not block updates, including normal template design refreshes by Notes.
* If the field is set to **Yes**, CIAO! ignores the template-linkage of the design element. In this case, as with any other design element, updates will be blocked unless you have the design element checked out.
