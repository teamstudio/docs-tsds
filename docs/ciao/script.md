# Overview

You can perform some CIAO! operations using LotusScript. Using the CIAO script library, which is included with CIAO! (**ciao.ntf**), you can do the following:

* Generate a list of changes based on the database that you specify and a range of version labels
* Generate a report of checkouts for each design element in the database  you specify using a description title for the report
* Create a version of the database specified
* Return the text string that is associated with a given error code

This section provides detailed descriptions of each CIAO! script library function, followed by agent examples that illustrate  how to use it.

The CIAO! script library exposes the following functions

| Function | Description |
| --- | --- |
| [CIAOCreateChangeList](scriptchangelist.md) | Generate a list of changes based on the database you specify and a range of version labels. |
| [CIAOCreateCheckoutReport](scriptcheckoutreport.md) | Generate a report of checkouts for each design element in the database you specify using a description title for the report. |
| [CIAODbCheckInNote2](scriptcheckinnote.md) | Check in a note. |
| [CIAODbCheckOutNote2](scriptcheckinnote.md) | Check out a note. |
| [CIAOMakeVersionImp](scriptmakeversion.md) | Create a version of the database specified. |
| [CIAOStringLoad](scriptstringload.md) | Return the text string associated with a given error code. |

If you work within the **ciao.ntf** template when testing or using the scripts, you will not have to worry about creating a CIAO! script library. However, if you move the scripts to a different database or template, you must also copy over this script library, possibly with its dependent script libraries.