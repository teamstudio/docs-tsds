# DEANStringLoadW32

## 説明
他の API 関数から返すエラーコードに関連づけられているエラーメッセージを取得します。

## シンタックス
```
status = DEANStringLoadW32( <Status>, <Message>, <MessageBufferSize> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| Status | 入力 | Long | いずれかの DEANxxx 関数から返された数値。 |
| Message | 出力 | String | nStatus コードに関連付けられたメッセージテキストを受け取る文字列。 |
| MessageBufferSize | 入力 | Long | 文字列の最大文字数です。 |

## 使用例
```vbscript
Dim szBuffer As String*255
status = DEANAnalyzeW32(...)
DEANStringLoadW32( status, szBuffer, 255 )
strErr = Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 ) '文字列をロータススクリプト文字に変換する
MessageBox strErr
```
