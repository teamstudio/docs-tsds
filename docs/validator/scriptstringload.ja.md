# LINKStringLoad

## 説明
API 関数から指定されたエラーコードに関連するテキスト文字列を返します。

## シンタックス
```
status = LINKStringLoad( <Status>, <Message>, <MessageBufferSize> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| Status | 入力 | Long | LINKxxx 関数により返される数値。 |
| Message | 出力 | String | Status コードに関連付けられたメッ セージテキストを受け取る文字列。 |
| MessageBufferSize | 入力 | Long | 文字列の最大文字数。 |

## 例
``` vbscript
Dim szBuffer As String*255
status = LINKGenerateReport(...)
LINKStringLoad( status, szBuffer, 255 )
strErr = Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 ) '文字列をロータススクリプト文字列に変換する
MessageBox strErr
```