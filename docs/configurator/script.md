# Overview

You can perform some Configurator operations from LotusScript. Use the Configurator script library which is included in the Teamstudio Reports template (**tmslogs.ntf**) to set up a search and replace configuration to be run in batch.

This section provides detailed descriptions of each Configurator script library function, followed by agent examples that illustrate how to use it.

The Configurator script library exposes the following functions:

| Function | Description |
| --- | --- |
| [CONFYFindAndReplace](scriptfar.md) | Performs a find and replace on a given database. Assumes default options for matching and will place the output results in a database created from **tmslogs.ntf**. Returns counts of occurrences found and replaced. |
| [CONFYFindAndReplaceEx](scriptfar.md) | Lets you use a selection formula to specify design elements to search. Assumes default options for matching and will place the output results in a database created from **tmslogs.ntf**. Returns counts of occurrences found and replaced. |
| [CONFYFindAndReplaceEx2](scriptfar.md) | Lets you pass a formula to specify design elements to search and also lets you specify the log database and document titles. Assumes default options for matching and will place the output results in a database created from **tmslogs.ntf**. Returns counts of occurrences found and replaced. |
| [CONFYCompileAndSign](scriptcompile.md) | Causes Configurator to recompile and re-sign design notes in the database using the ID of the user running the agent. |
| [CONFYStringLoad](scriptstringload.md) | Obtains the error message associated with an error code returned from the other APIs. |