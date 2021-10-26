# Overview

CIAO! stores a history of design element changes and application template releases in the Log database. The database can store the history of a single application template, a group of templates (a project) or a group of projects.

Each time you check in a design element, CIAO! writes a copy of the design element to the log database you have specified in the CIAO! Configuration Database.

CIAO! also writes to this log when a new application template is released. In this case, CIAO! labels the design elements in the log and creates a new database version document. 

The history for each element consists of the following:

* Developer who checked in the item or created the application release
* Date and time operation was performed
* Name of the design element as shown in the Notes design pane at the time the item was checked in
* Comment written by the developer describing the check-in or version
* Version label
* Version number
* Issues

The history for database version documents consists of the following:

* The ODS version with which the version database was created
* The actual database, stored as an attachment
* The original filename of the attachment before it was renamed to the version.nsf or version.zip