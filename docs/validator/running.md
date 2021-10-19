# Running Validator

To run Validator, you first set options and parameters and then you specify the output database's server name and path.

## To run Validator
1. Set the following Validator options:  
   <table><tr><th>Options</th><th>Description</th></tr>
     <tr><td>Report All Links</td><td>This will generate report documents for all doclinks, good or bad. Selecting this option disables the **No Warnings** and the **Don't Check URLs** options.</td></tr>
     <tr><td>No Warnings</td><td>Validator will not report errors that are classified as warnings; for example, hotspots with no link specified.</td></tr>
     <tr><td>Don't Check URLs</td><td>Validator will not check URLs. Do not try to check URLs if you are not connected to the internet.</td></tr>
     <tr><td>No External Links</td><td>If you select this option, Validator will report as an error any link that doesn't point to the current database.</td></tr>
     <tr><td>Assume Replicas are local</td><td>If you select this option, Validator will not look at replica databases on external servers.</td></tr>
     <tr><td>Don't check fields</td><td>Validator does not check for field errors.</td></tr>
     <tr><td>Don't check keyword fields</td><td>Validator ignores keyword fields.</td></tr>
     <tr><td>Ignore empty fields</td><td>Validator ignores empty fields (fields on documents with no data).</td></tr>
     <tr><td>Don't check Conflicts</td><td>Validator does not check conflicts.</td></tr>
   </table>
2. You can set Validator to report on design elements or documents or both. If you set Validator to report on documents, you must specify *By Formula* or *By View*.
    -  If you specify *By Formula*, @ALL appears as the default. You can enter a valid selection formula for your search.
    -  If you specify *By View*, available views appear in the dropdown list, allowing you to select one of the views in the source database.
3. Enter the server name and path of the Reports database (Output).
4. Click Run to create the Reports database.  
   Validator will create the Reports database and automatically open it.
   <div class="admonition">
   <p class="admonition-title">Info</p>
   <ul>
     <li>Pressing <strong>CTRL-BREAK</strong> while Validator is running will cause Validator to halt in place and open the report database.</li>
     <li>When the output database does not exist, you see the <strong>Create New Log Database</strong> window where you can enter the new <strong>Database Title</strong>.</li>
     </ul>
   </div>