# CIAOCreateChangeList

## 説明
指定したデータベースおよびバージョンラベルの範囲に基づいて、変更の一覧を生成します。

## シンタックス
```
status = CIAOCreateChangeList( <SourcePath>, <OutputPath>, <OutputTitle>, <NewerVersion>, <OlderVersion>, <Flags> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| SourcePath | 入力 | String | 処理するノーツデータベースのパスです。サーバー名とパス名は !! で区切ります。このデータベースは CIAO! の監視下に置かれ、CIAO! の 設定データベースで指定されている正しいログデータベースが設定されている必要があります。 |
| OutputPath | 入力 | String | CIAO! によるレポートの書き出し先データベースのパスです。サーバー名とパス名は !! で区切ります。このデータベースが存在しない場合は、CIAO! によって作成されます。 |
| OutputTitle | 入力 | String | レポートの出力データベースのタイトルです。 |
| NewerVersion | 入力 | String | 検索するバージョンラベル範囲の終わりの指 定に使用します。現在のラベル ( データベースの現在の状態 ) を指定するには、"" ( 空の引用符 ) を使用します。 |
| OlderVersion | 入力 | String | 検索する 2 つ目のラベルの指定に使用します。 |
| Flags | 入力 | Long | レポートに出力する内容を制御するフラグです。0 または下記のフラグの組み合わせを渡すことができます。複数のフラグを使用する場合はプラス記号(+) を組み合わせて使用します。 |

## フラグ
| フラグ | 説明 |
| --- | --- |
| CIAO_REPORT_SILENT | ステータスバーを非表示にします。 |
| CIAO_CL_REPORT_DELTA | レポートに相違を含めます。 |
| CIAO_CL_REPORT_OWNER | 要素をチェックインしたユーザーを含めます。 |
| CIAO_CL_REPORT_DATE | 要素がチェックインされた日付を含めます。 |
| CIAO_CL_REPORT_COMMENT | チェックインコメントを含めます。 |
| CIAO_CL_REPORT_IGNORE_NO_PREV | 過去にチェックインが行われていない要素を無視します。 |
| CIAO_CL_REPORT_DEFAULT | ステータスバーを非表示にします。レポートの相違点、要素をチェックインしたユー ザーの識別情報、要素がチェックインされた日付、チェックインコメントを含めます。 |
 
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
status = CIAOCreateChangeList( strPath, "CIAO\\Reports.nsf", "CIAO Change List", "", "BASELINE", CIAO_CL_REPORT_DEFAULT )
If status <> 0 Then
    Dim szBuffer As String*255
    CIAOStringLoad status, szBuffer, 255
    MessageBox Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 )
End If
```