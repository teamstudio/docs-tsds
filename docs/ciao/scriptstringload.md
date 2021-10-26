# CIAOStringLoad

## Description
Obtains the error message associated with any error code returned from other API functions.

## Syntax
```
status = CIAOStringLoad( <Status>, <Message>, <MessageBufferSize> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| Status | Input | Long | The numeric value returned by one of the DEANxxx functions. |
| Message | Output | String | This is a string that will receive the message text associated with the status code. |
| MessageBufferSize | Input | Long | This is the maximum size that the string should be. |

## Example
```
Dim szBuffer As String*255
CIAOStringLoad( status, szBuffer, 255 )
strErr = Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 ) 'Convert the string to a LotusScript string
MessageBox strErr
```