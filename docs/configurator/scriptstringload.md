# CONFYStringLoad

## Description
Obtains the error message associated with any error code returned from other API functions.

## Syntax
```
status = CONFYStringLoad( <Status>, <Message>, <MessageBufferSize> )
```

## Parameters
| Parameter | Input/Output | Type | Description |
| --- | --- | --- | --- |
| Status | Input | Long | The numeric value returned by one of the CONFYxxx functions. |
| Message | Output | String | This is a string that will receive the message text associated with the status code. |
| MessageBufferSize | Input | Long | This is the maximum size that the string should be. |

## Example
```vbscript
Dim szBuffer As String*255
status = CONFYFindAndReplace(...)
CONFYStringLoad( status, szBuffer, 255 )
strErr = Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 ) 'Convert the string to a LotusScript string
MessageBox strErr
```