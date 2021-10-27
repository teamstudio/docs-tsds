# Running Promotions

## Promoting Databases
To run a promotion, select the desired promotion path in one of the Promotion Path views in the CIAO! configuration database, and click the **Promote** action. CIAO! will promote the database, running each enabled promotion step defined for the promotion.

When the promotion is complete, the promotion log will be displayed.

!!! note 
    Teamstudio CIAO! runs promotions in the Notes Client environment - Access is blocked to the Notes client while promoting an application. Users who frequently run complex promotions may benefit from Teamstudio Build Manager, which runs promotions in a separate process, without blocking the client. For more information on Build Manager, contact your Account Manager, or see [Product Comparison - CIAO! and Build Manager](promotioncompare.md)
 
## Promoting Multiple Databases
CIAO! can promote more than one database in two ways:

* By selecting multiple promotion paths before clicking "Promote." CIAO! will run all selected promotions, however, the order in which promotions runs is not guaranteed.
* By creating and running **Project Builds**. Project Builds allow defining a repeatable collection of promotions to run in a particular order. For more information, see [Project Builds](promotionproject.md).
