# Synchronizing

Use the **Database > Synchronize Design** command to copy all new or changed design elements from a template into a database.

If the database inherits at the database level, then when you synchronize you'll see options to synchronize **Database Options**, **ACL**, and **Replication Settings**. The **Synchronize Design** command considers the date and copies design elements that are new or have changed.

This functions differently than Notes design replace/refresh, as follows:

* When synchronizing designs, matches are made based on a design note's name and type. If there is more than one note with the same name and type, the UNID is checked. If the UNID doesn't match, then the unmatched design note is added to the database.
* All of the database options are synchronized except those that are template-specific including the **List as Advanced Template in 'New Database'** window, **Copy profile documents with design**, **Single copy template**; unlike design/refresh where only the specific elements are synchronized.
 