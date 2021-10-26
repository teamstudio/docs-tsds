# About the Log Database ACL

The ACL of the log database should be set so that any CIAO! user (including the server, if you are using CIAO! Server Edition) has author-level access or better with the Create Documents attribute set. CIAO! creates a document in the log database for every check-in operation. 
 
!!! note
    *Do not edit any of the entries in the Log database using the Notes client.*  
    Because the log database entries contain actual copies of the design elements, which the Notes client is not expecting, these will not be written out correctly, and will therefore cause problems with CIAO! later on.  
    The Log database is intended to be read-only, and should not, under any circumstances, be changed using the Notes client.
