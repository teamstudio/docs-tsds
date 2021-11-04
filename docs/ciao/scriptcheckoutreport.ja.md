# CIAOCreateCheckoutReport

## 説明
レポートの内容を説明するタイトルを使用して、指定したデータベースの各設計要素のチェックアウトレポートを作成します。

## シンタックス
```
status = CIAOCreateCheckoutReport( <SourcePath>, <OutputPath>, <OutputTitle>, <Description> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| SourcePath | 入力 | String | 処理するノーツデータベースのパスです。サーバー名とパス名は !! で区切ります。このデータベースは CIAO! の監視下に置かれ、CIAO! の 設定データベースで指定されている正しいログデータベースが設定されている必要があります。 |
| OutputPath | 入力 | String | CIAO! によるレポートの書き出し先データベースのパスです。サーバー名とパス名は !! で区切ります。このデータベースが存在しない場合は、CIAO! によって作成されます。 |
| OutputTitle | 入力 | String | Theレポートの出力データベースのタイトルです。 |
| Description | 入力 | String | レポートのタイトルを示します。 |

## 戻り値
| 戻り値 | 型 | 説明 |
| --- | --- | --- |
| status | Long | 0 は、エラーが発生しなかったことを示します。戻り値が 0 で ない場合は、 [CIAOStringLoad](scriptstringload.md) を使用して、エラーコードに関連するエラーメッセージを取得してください。 |

## 例
```vbscript
Dim status As Long
Dim strPath As String
strPath = ""
If strDatabaseServer <> "" Then
    strPath = strDatabaseServer + "!!"
End If
strPath = strPath + strDatabasePath
status = CIAOCreateCheckoutReport( strPath, "CIAO\\Reports.nsf", "CIAO Checkout Report", "Sample Title" )
If status <> 0 Then
    Dim szBuffer As String*255
    CIAOStringLoad status, szBuffer, 255
    MessageBox Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 )
End If
```