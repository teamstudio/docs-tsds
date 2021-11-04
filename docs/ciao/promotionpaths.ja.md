# 紹介

Promotion Paths define targets for moving source templates to new environments when [データベースの昇格](promoting.md).

Two types of CIAO! documents form the basis for building and promoting databases using CIAO!:

* Database Documents, also called CIAO! Configuration or "Watch" documents, define the "source" location - the source template of an application where development takes place.
* Promotion Paths define a "target" location - a server and path where the source template should be copied; build steps can then be run against this target to prepare it for release.

<figure markdown="1">
  ![Promotion Paths](img/promotionpaths.png)
</figure>

 
## Database Documents
Configuration documents are created by CIAO! when a source database is placed under CIAO! control, as described in [CIAO! の使用](using.md) For information on configuring database documents, see [CIAO! 設定情報について](configbasics.md).

For promotions, CIAO! uses the Database Document to identify the source template which the build will copy and act on, and can be created:

* By choosing the **CIAO!** view menu button and choosing **Add Database** to add a source template that exists on a server.
* By launching the CIAO! client on a currently unwatched database, and following the prompts to begin watching the database.

The second method will help ensure that all required fields are set accurately.
 
## Promotion Paths
Promotion Paths specify a target location to "promote" a template.  Promotion paths copy the source template to the target location, and run the child Build Steps against the new copy.  Typically, a Promotion Path will include a child **Build Step** to refresh the design of one or more databases in the environment (e.g. QA, UAT, Production) where the template has been copied, or "promoted."

To create a Promotion Path, select the Database document that identifies the source template, and choose **Create > Promotion Path**. 
 
## Build Steps
Promotion Paths create or update a template in the target environment. By creating additional **Build Steps** for a promotion path, CIAO! can be configured to reliably prepare the template for deployment (for example, set the template name and sign design elements) and deploy it by refreshing the design of target databases. For more information, see [Build Steps](buildsteps.md).
