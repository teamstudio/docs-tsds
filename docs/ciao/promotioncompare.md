# Product Comparison - CIAO! and Build Manager

The Teamstudio CIAO! configuration database contains **Promotion** functionality and **Build Steps** that are a subset of the functionality available in Teamstudio Build Manager.

The Promotion features included with CIAO! are intended to provide developers and administrators the capability of standardizing and automating the deployment of typical Notes applications, producing repeatable builds with relatively low complexity in configuration.

Teamstudio Build Manager includes several additional capabilities to manage complex deployments and providing support for more advanced environments. Build manager includes functionality to work with multi-stage release processes (test/QA/UAT), release management, approval processes, and deployment tracking.

The following table highlights the key features of each product. For more information on Build Manager, see the Build Manager online [documentation](/docs-bm), contact your account manager, or email us at [techsupport@teamstudio.com](mailto:techsupport@teamstudio.com).
  
| Feature | CIAO! | Build Manager | Description |
| --- | --- | --- | --- |
| Promote | ✅ | ✅ | Deploy template to servers |
| Make Version* | ✅ | ✅ | Create a new CIAO! version.<br>*Requires CIAO! |
| Design Audit** | ✅ | ✅ | Run Analyzer Audit filters to ensure standards are met<br>**Requires Analyzer. |
| Database Properties | ✅ | ✅ | Set template name, title, and other template properties |
| ACL | ✅ | ✅ | Define ACL for promoted template |
| Search/Replace*** | ✅ | ✅ | Search and Replace text with Configurator<br>***Requires Configurator. |
| Copy Database | ✅ | ✅ | Create a copy of the template in another location |
| Element Properties | ✅ | ✅ | Change element-level properties such as element-level inheritance, design refresh prohibition |
| Compile LotusScript | ✅ | ✅ | Compile LotusScript to ensure validity and avoid runtime errors |
| Sign Design | ✅ | ✅ | Sign template with an ID stored in CIAO!/Build Manager |
| Refresh Design | ✅ | ✅ | Refresh the design of applications based on the current template |
| Run Agent | | ✅ | Run an agent in any database, optionally passing parameters |
| Create Test Data | | ✅ | Reset baseline data for Test, QA or UAT environments |
| Run Shell Command | | ✅ | Execute OS command line operations, capture and validate command output |
| Send Console Command | | ✅ | Send remote Domino console commands to a server |
| Set Agent Server | | ✅ | Set agent “run on server” setting |
| Enable Agent | | ✅ | Set agent “enabled” status |
| Set Agent Behalf-Of | | ✅ | Set agent “Run on behalf of” setting | 
| Switch ID | | ✅ | Switch to an ID stored in CIAO!/Build Manager before running subsequent steps |
| Approval Workflow | | ✅ | Require approvals prior to allowing promotions to certain environments |
| Release Management | | ✅ | Store versions of template and track status and deployment in a Template Registry database |
| Promote As ID | | ✅ | Run promotion using an ID stored in CIAO!/Build Manager, for elevated access levels/permissions |
| Background Promotions | | ✅ | Promotions run in a separate process, freeing the Notes client for the user |
