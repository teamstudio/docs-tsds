# CONFYStringLoad

## 説明
API 関数から返されたエラーコードに関連したエラーメッセージを取得します。

## シンタックス
```
status = CONFYStringLoad( <Status>, <Message>, <MessageBufferSize> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| Status | 入力 | Long | いずれかの CONFYxxx 関数から返された数値です。 |
| Message | 出力 | String | Status コードに関連付けられたメッセージテキストを受け取る文字列です。 |
| MessageBufferSize | 入力 | Long | 文字列の最大文字数です。 |

## 例
```vbscript
Dim szBuffer As String*255
status = CONFYFindAndReplace(...)
CONFYStringLoad( status, szBuffer, 255 )
strErr = Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 ) '文字列をロータススクリプト文字列に変換する
MessageBox strErr
```