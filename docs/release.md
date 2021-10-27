# Release Notes

Edition 33 is a feature release of the Teamstudio Notes tools. In addition to fixing a number of bugs, this release contains significant enhancements to the Teamstudio CIAO! features that assist in preparing templates for deployment, along with updates to all of the database templates (NTFs) used by the tools for reporting and configuration. This document describes these enhancements, along with a list of specific fixes.

## CIAO! Promotion Features
Teamstudio CIAO! now includes new features to help ensure accurate, repeatable application builds.

CIAO! has long offered a **Promotion** feature via the CIAO! Configuration database. This feature supports creating **Promotion Paths** for templates watched by CIAO! that define server and file locations where the template should be deployed. Promoting a template creates a copy of the template at the desired location, and also supports an optional **Build Step** to create a CIAO! version of the template automatically prior to the deployment.

Edition 33 adds several new **Build Steps** to make it easy to prepare templates for deployment in a repeatable, consistent, and self-documenting manner – all with a single click. Similar to build systems for other types of software development, these new features help ensure each new version of a template is properly prepared for release without requiring a manual process or checklist.

Significant new **Build Steps** include:

* Setting template properties such as Design Template Name and Title
* Defining the template ACL
* Changing element properties, such as clearing element-level design inheritance and Prohibit Design Refresh settings
* Compiling all LotusScript
* Signing the template with a specific ID
* Refreshing the design of target application(s) from the new template

Detailed descriptions of the available functions are available from the [Build Steps](ciao/buildsteps.md) page. For more information on **Promotions** in general, see [Promotion Paths](ciao/promotionpaths.md).

The new **Build Steps** represent a subset of the features available in Teamstudio Build Manager, which offers many additional capabilities to manage complex builds, including the ability to promote using different Notes IDs to support segregation of duties, Release Management/Deployment Tracking features, and Approval workflows. For a comparison of CIAO! and Build Manager, see [Product Comparison - CIAO! and Build Manager](ciao/promotioncompare.md).

## Upgrading CIAO! Configuration Database
The updated Edition 33 CIAO! Configuration database is designed to continue working with existing **Promotion Paths**. A minor upgrade process is required, due to additional features added to the product.

Prior versions of the CIAO! configuration database allowed free-form entry of the target server specified in the **Promotion Path** document, without any validation. The current version requires that target servers for promotion and design refresh actions be defined as **Stored Servers**, under the **Resources** tab in the configuration UI. **Stored Server** definitions can only be created by users with the [[Admin]] ACL role, and contain additional settings including defining which users are allowed to promote databases to the target server, and what other servers may be used as **Design Refresh** targets. For more information, see [Stored Servers](ciao/storedservers.md).

To assist in the upgrade process, the CIAO! configuration now includes an agent available via **Actions > Admin > Verify Stored Servers**. This agent launches a wizard to scan **Promotion Paths** and **Design Refresh** steps and display the names of servers that have missing or disabled **Stored Server** definitions. Server names can be selected to automatically create **Stored Server** documents.

Upgrading from a prior CIAO! template involves:

* Signing the new CIAO! Configuration and CIAO! Log templates with an appropriate Notes ID
* Refreshing the design of all CIAO! configuration and CIAO! log databases
* Running the **Verify Stored Servers** action to create server definitions as needed (only required if **Promotion Paths** are in use in prior version)

For more information on the **Verify Stored Servers** action, see [Stored Servers](ciao/storedservers.md).

## Template Updates
The Teamstudio Notes Tools utilize several Notes application templates for configuration and reporting. All templates have updated for Edition 33, including updated UI look and feel and new icons.  Several templates also include usability improvements.

## Fix List
### 33.0.4
[TMS-1437] - Update code signing certificates to replace expiring certificates for the installer and Java plugins

### 33.0.3
[TMS-1286] - CIAO change report can fail to list all changes if Notes application has been moved  
[TMS-1302] - Installer does not detect Notes program locations on a clean Notes 11 install  
[TMS-1306] - The tools installer cannot uninstall if Notes has been moved or upgraded to a new location  
[TMS-1348] - Code copied from Configurator loses new lines when pasted into Notes   
[TMS-1366] - CIAO! configuration database should allow blank target filename in Promotion Path (to promote with source filename)  
[TMS-1380] - Analyzer always displays database percent usage as 0%  
[TMS-1381] - Analyzer displays database space allocated and space free incorrectly for databases > 4GB  
[TMS-1390] - Analyzer can crash evaluating formulas with large numbers of @if statements  

### 33.0.2
[TMS-1266] - Delta crash running a report  
[TMS-1281] - Analyzer writes 'Filter error: Out of Memory' to the audit log for large minified documents  
[TMS-1300] - The message displayed for an expired key incorrectly refers to 'demonstration software'  

### 33.0.1
[TMS-1247] - Update code signing certificates to replace expiring certificates for the installer and Java plugins  
[TMS-1249] - Fix Launch CIAO! action in CIAO! Configuration database  
[TMS-1250] - Fix Analyzer Filters Severity Definition sorting and lookup issues - upgrade existing   Filters database designs to the latest template to use with the CIAO! Design Audit step  

### 33.0.0
[TMS-109] - Reports views should sort date chronologically not alphabetically  
[TMS-240] - Analysis Form properties section shows red text that should be hidden  
[TMS-959] - Analyzer crashes intermittently on very large script libraries  
[TMS-1059] - Analyzer does not write computed labels in outline entries  
[TMS-1167] - CIAO! crashes intermittently while checking design elements in or out in Designer  
[TMS-1217] - Add serial key expiration dates to the about dialog  
[TMS-1220] - Analyzer reports are missing XPage and Page options for database Launch settings  
[TMS-1222] - CIAO! intermittently displays "command not available" error on opening  
[TMS-1225] - CIAO! View action to enable/disable steps should clarify it does not affect CIAO! configuration documents  
[TMS-1238] - CIAO does not list available versions correctly when a database is moved to a new path or server