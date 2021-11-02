# DIFFStringLoadW32

## 説明
API 関数から返されたエラーコードに関連付けられているエラーメッセージ を取得します。

## シンタックス
```
status = DIFFStringLoadW32( <Status>, <Message>, <MessageBufferSize> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| Status | 入力 | Long | いずれかの DIFFxxx 関数により返された 数値です。 |
| Message | 出力 | String | Status コードに関連付けられたメッセージテキストを受け取る文字列です。 |
| MessageBufferSize | 入力 |	Long | 文字列の最大文字数です。 |

## 例
```vbscript
Dim szBuffer As String*255
status = DIFFReportW32(...)
DIFFStringLoadW32( status, szBuffer, 255 )
strErr = Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 ) '文字列をロータススクリプト文字列に変換する
MessageBox strErr
```