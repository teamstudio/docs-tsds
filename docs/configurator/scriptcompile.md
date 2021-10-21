# CONFYCompileAndSign

## Description
Causes Configurator to recompile and re-sign all notes in the database using the ID of the user running the agent.

## Syntax
```
status = CONFYCompileAndSign( <SourceDatabasePath>, <Flags> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| SourceDatabasePath | Input | String | The path to the database that you want to precess. Separate the server and pathname with !! |
| Flags | Input | Long | A combination of the CONFY_COMPILE_SIGN_xxx flags below. |

## Flags
| Flag | Description |
| --- | --- |
| CONFY_COMPILE_SIGN_DEFAULT | The default behavior is to compile all design notes that are unsigned, including agents. Normally this will only be notes that have been modified by Configurator. |
| CONFY_COMPILE_SIGN_ALLBUTAGENTS | Includes everything except agents. |
| CONFY_COMPILE_SIGN_AGENTS | Includes agents.<br>Note: Signing an agent may affect its ability to run from a server. See your Notes Application Development reference documentation for information on running agents on clients and servers. |
| CONFY_COMPILE_SIGN_UNSIGNED | Processes only design notes that are unsigned - usually notes that have been changed by Configurator. |
| CONFY_RUN_SILENT | Do not display the status bar. |

## Return Value
| Return value | Type | Description |
| --- | --- | --- |
| status | Long | Zero (0) indicates that no error has occurred. If the return value is non-zero, use [CONFYStringLoad](scriptstringload.md) to get the error message associated with the error code. |

## Example
```vbscript
status = CONFYCompileAndSign(
    "myserver!!dbtorun.nsf",_
    "CONFY_COMPILE_SIGN_ALLBUTAGENTS + CONFY_COMPILE_SIGN_UNSIGNED)
```