# Overview

Teamstudio CIAO! allows multiple people to work on the design of the same database at the same time, without generating save conflicts on the particular design elements they are working on. You can use CIAO! client and CIAO! server for version control and for promoting versions of your database through the development cycle. 

!!! note
    All developers must use CIAO! for design element locking to work properly. 

If you have used a version control system, for example, Subversion, which is an open-source source-control system, you are likely familiar with the principle of check-in/out. By checking out design elements, you lock those elements so no one else can change them while you are working on them.

CIAO! is made up of the CIAO! client, the CIAO! Configuration database, and the CIAO! Log database. The CIAO! client is where you check in and out the design elements you are working with. The CIAO! Config database is a list of databases that CIAO! knows about. With the CIAO! Config database, you can configure database promotion and version numbering, set up user authority for various CIAO! features, and link CIAO! with your issue tracking database. The CIAO! Log database keeps the history of every design element checked in. 