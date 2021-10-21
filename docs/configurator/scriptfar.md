# CONFYFindAndReplace

## Description
The three CONFYFindAndReplace functions perform find and replace on a given database. They all place the output results in a database created from **tmslogs.ntf** and return counts of occurrences found and replaced. They differ only in that the Ex and Ex2 variants give you more options to control the operation.

## Syntax
### CONFYFindAndReplace
```
status = CONFYFindAndReplace( <SourceDb>, <LogDb>, <FindText>, <ReplaceText>,
    <MatchFlags>, <SearchFlags>, <RunFlags>, <SelectionString>, <FilterString>,
    <Searched>, <Found>, <Replaced> )
```
      
### CONFYFindAndReplaceEx
```
status = CONFYFindAndReplaceEx( <SourceDb>, <LogDb>, <FindText>, <ReplaceText>,
    <MatchFlags>, <SearchFlags>, <RunFlags>, <SelectionString>, <DesignSelectionString>,
    <FilterString>,   <Searched>, <Found>, <Replaced> )
```

### CONFYFindAndReplaceEx2
```
status = CONFYFindAndReplaceEx2( <SourceDb>, <LogDb>, <LogDbTitle>, <DocTitle>,
    <FindText>, <ReplaceText>, <MatchFlags>, <SearchFlags>, <RunFlags>,
    <SelectionString>, <DesignSelectionString>, <FilterString>,
    <Searched>, <Found>, <Replaced> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| SourceDb | Input | String | The database that you want to search. Separate the server and pathname with !! |
| LogDb | Input | String | The output database for the log. Separate the server and pathname with !! Configurator will create this database if it does not exist. |
| LogDbTitle | Input | String | **CONFYFindAndReplaceEx2 only.** The title to use if the log database needs to be created. A default title ("Confy Report") will be used if this is blank (""). |
| DocTitle | Input | String | **CONFYFindAndReplaceEx2 only.** The title to use for log documents. A default title will be generated if this is blank (""). |
| FindText | Input | String | The text that you want to find. |
| ReplaceText | Input | String | The text that should replace the find text. |
| MatchFlags | Input | Long | One of more of the CONFY_MATCH_xxx constants listed below. Combine multiple flags with the plus sign (+). |
| SearchFlags | Input | Long | One or more of the CONFY_SEARCH_xxx constants listed below. Combine multiple flags with the plus sign (+). |
| RunFlags | Input | Long | One or more of the CONFY_RUN_xxx constants listed below. Combine multiple flags with the plus sign (+). |
| SelectionString | Input | String | Used to specify the selection formula or view when searching data documents.<br>If you only specify the CONFY_SEARCH_DATA flag, this parameter should contain a selection formula identifying the documents to be searched. If you **also** specify CONFY_SEARCH_BYVIEW, this parameter should contain the name of the view containing the documents to be searched. |
| DesignSelectionString | Input | String | **CONFYFindAndReplaceEx** and **CONFYFindAndReplaceEx2** only. Used to specify a selection formula when searching design notes. CONFY_SEARCH_DESIGN must be passed as one of the search flags. |
| FilterString | Input | String | A [Context Filter](../analyzer/scriptctxfilter.md) to limit the search to certain types of design notes. Use the empty string, "", to search all design note types. |
| Searched | Output | Long | Returns the number of documents that were searched. |
| Found | Output | Long | Returns the number of times the search text was found. |
| Replaced | Output | Long | Returns the number of times the search text was replaced. |

## Match Flags
| Flag | Description |
| --- | --- |
| CONFY_MATCH_DEFAULT | None of the following flags are set. |
| CONFY_MATCH_WHOLEWORD | Turns on whole word searching. |
| CONFY_MATCH_ACCENT | Turns on accent-sensitive searching. |
| CONFY_MATCH_CASE | Turns on case-sensitive searching. |
| CONFY_MATCH_WILDCARD | Search string contains wildcard characters. |
| CONFY_MATCH_REGEXP | Search string is a regular expression. |

## Search Flags
| Flag | Description |
| --- | --- |
| CONFY_SEARCH_DEFAULT | The default behavior is to search the design only and not perform any replacements. |
| CONFY_SEARCH_DESIGN | Search design elements. |
| CONFY_SEARCH_DATA | Search data documents, identified by a selection formula. |
| CONFY_SEARCH_BYVIEW | Modifies CONFY_SEARCH_DATA to identify documents by view rather than formula. |
| CONFY_SEARCH_MODE_REPLACE | Actually performs replacements. Without this flag Configurator will only search. |

## Run Flags
| Flag | Description |
| --- | --- |
| CONFY_RUN_DEFAULT | Default operation. Configurator will not recompile LotusScript and will re-sign any design elements that are changed. |
| CONFY_RUN_COMPILE | Recompile any design elements that Configurator changes. |
| CONFY_RUN_NO_SIGN | Don't re-sign any notes. |
| CONFY_RUN_SILENT | Don't display the status bar. |
| CONFY_RUN_DOC_PER_NOTE | For each design element or document searched, generate a single log document with the details of what was found and replaced. If you don't use this flag, all the information will be stored in a single document which may be difficult to work with if there are a large number of search matches. |

!!! note
    When doing multiple search and replace operations on the same database, compiling and signing the same element multiple times is expensive. You can save processing time by waiting to do all the signing at once. To do this, specify the CONFY_RUN_NO_SIGN flag and do not specify CONFY_RUN_COMPILE. Then call the [CONFYCompileAndSign](scriptcompile.md) function once all the search and replace operations are done.
    
## Return Value
| Return value | Type | Description |
| --- | --- | --- |
| status | Long | Zero (0) indicates that no error occurred. If the return value is non-zero, use [CONFYStringLoad](scriptstringload.md) to get the error message associated with the error code. |

## Examples
### CONFYFindAndReplace
```vbscript
status = CONFYFindAndReplace(_
    strSourceDatabase,_
    "confrep.nsf",_ 'Log database for output
    "Teamstudio",_ 'Text to find
    "TS",_ 'Text to replace
    CONFY_MATCH_DEFAULT,_ 'Default match options for case/accent etc
    CONFY_SEARCH_DESIGN + CONFY_SEARCH_MODE_REPLACE,_ 'Search design and perform replace
    CONFY_RUN_COMPILE,_ 'Recompile modified design notes
    "",_ 'Data selection formula, not used
    "",_ 'Context filter, default includes all design element types
    numSearched,_ 'Output parameter to receive number of documents searched
    numFound,_ 'Output parameter to receive number of matches found
    numReplaced) 'Output parameter to receive number of replacements made
```

### CONFYFindAndReplaceEx
```vbscript
status = CONFYFindAndReplaceEx(_
    strSourceDatabase,_
    "confrep.nsf",_ 'Log database for output
    "teamstudio",_ 'Text to find
    "Teamstudio",_ 'Text to replace
    CONFY_MATCH_CASE,_ 'Case sensitive match
    CONFY_SEARCH_DESIGN + CONFY_SEARCH_DATA + CONFY_SEARCH_MODE_REPLACE,_ 'Search design and data and perform replace
    CONFY_RUN_COMPILE,_ 'Recompile modified design notes
    "SELECT @All",_ 'Data selection formula
    |$Title="MainForm"|,_ 'Design selection formula, search elements named MainForm
    "-FM",_ 'Context filter, only search forms
    numSearched,_ 'Output parameter to receive number of documents searched
    numFound,_ 'Output parameter to receive number of matches found
    numReplaced) 'Output parameter to receive number of replacements made
```
    
### CONFYFindAndReplaceEx2
```vbscript
status = CONFYFindAndReplaceEx2(_
    "server!!dbToSearch.nsf",_ 'Database to search
    "confrep.nsf",_ 'Log database for output
    "Configurator Report",_ 'Title for log database if created
    "Replace performed on server!!dbToSearch.nsf",_ 'Title for log documents
    "teamstudio",_ 'Text to find
    "Teamstudio",_ 'Text to replace
    CONFY_MATCH_CASE,_ 'Case sensitive search
    CONFY_SEARCH_DESIGN + CONFY_SEARCH_DATA + CONFY_SEARCH_MODE_REPLACE,_ 'Search design and data and perform replace
    CONFY_RUN_COMPILE,_ 'Recompile modified design notes
    "SELECT @All",_ 'Data selection formula
    |$Title="MainForm"|,_ 'Design selection formula, search elements named MainForm
    "-FM",_ 'Context filter, only search forms
    numSearched,_ 'Output parameter to receive number of documents searched
    numFound,_ 'Output parameter to receive number of matches found
    numReplaced) 'Output parameter to receive number of replacements made
```