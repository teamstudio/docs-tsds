# Configuring Undo

## To configure tracking of all NTF files
Undo automatically keeps track of changes for all NTF files you work with, whether on your local computer, or on a server, so you don't have to configure that. If you are wondering if Undo knows about your NTF file - no worries - it does!

If you prefer, you can manually configure Undo to keep track of changes to NSF files, or to keep track of changes within the files or folders you choose. 

## To configure tracking of all NSF files or only selected databases or folders
1. In a text editor, open the **Teamstudio.ini** file, which is located in the data directory.
2. In the [Undo] section, change the line that says "IncludeFiles=*.ntf" as follows:

| To track the following | Change "IncludeFiles" line as follows |
| --- | --- |
| All NSF files only | IncludeFiles=*.nsf |
| All NTF and all NSF files | IncludeFiles=.ntf,.nsf |
| Just a few databases you want, for example, mytest1.ntf and mytest2.ntf | IncludeFiles=mytest1.ntf,mytest2.ntf |
| One directory only, for example, the mail folder | IncludeFiles=mail/* |

!!! note
    Teamstudio recommends you only modify the IncludeFiles line if you have a very good reason. By leaving the default, you don't have to try to remember to add a new database or update the line again for a database whose name has changed.
