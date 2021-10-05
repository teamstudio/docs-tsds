# Analyzer Sample Agents

You can find sample agents in the Teamstudio Reports template You can find sample agents in the Teamstudio Reports template **tmslogs.ntf**, which is provided with the product. Run them as provided to see how they work. They demonstrate how to call Analyzer dynamically, whether real-time or on a scheduled basis.

As standard Notes agents coded in LotusScript, they have the same basic structure. First, they determine the files to be analyzed and the output analysis file to be created. Then they call an DeanAnalyze function to start Analyzer processing.

The function calls pass the file and other necessary parameters. The Analyzer script library contains the constant and function definitions necessary to start Analyzer.

You will likely want to change these agents to provide the pertinent file and path data. You can change, or copy and then change the agents. The script library and agents (with your modifications, if any) must be present in the database for which you will run the agent.

!!! note
    Do not change the Declaration section as doing so may cause the script library to malfunction.
    
## Analyzer Scripting Sample with Dialog
This agent prompts you to enter the name of the input file and the analysis output file. It uses a hidden form, *Analyzer Scripting Sample Dialog* that has the alias *AnalyzerDialog* in a DialogBox call to retrieve the file data.

You can use the function to supply the information about the file to be analyzed when you run the agent. You could also get this data using other techniques such as reading an input file or by searching the Notes directory on a server of local machine.

## Analyzer Scripting Sample - Directory Contents Analyzer
This agent illustrates how to gather the file information dynamically from a server and then call Analyzer. It shows how to match files by type. You could change this example to search for file names or directories that meet the criteria you supply.
