# CIAOMakeVersionImp

## 説明
指定したデータベースのバージョンを作成します。

## シンタックス
```
status = CIAOMakeVersion( <SourcePath>, <VersionLabel>, <Comment>, <VersionFlags>, <Flags> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| SourcePath | 入力 | String | 処理するノーツデータベースのパスです。サーバー名とパス名は !! で区切ります。このデータベースは CIAO! の監視下に置かれ、CIAO! の設定データベースで指定されている正しいログデータベースが設定されている必要があります。 |
| VersionLabel | 入力 | String | バージョン作成処理で使用されるバージョン ラベル。この文字列を空白にすることはできません。 |
| Comment | 入力 | String | バージョンコメントです。 この文字列は、 CIAO! 設定データベースでコメント強制が設定されていない場合にのみ、空白にすることができます。 |
| VersionFlags | 入力 | Long | 新しいリリースのバージョン番号の変更を制御するためのフラグです。 |
| Flags | 入力 | Long | レポートの内容を制御するためのフラグです。 |

## バージョンフラグ
| フラグ | 説明 |
| --- | --- |
| CIAO_MVERSION_NO_BUMP | バージョン番号を変更しません。 |
| CIAO_MVERSION_BUMP_MAJOR | メジャーバージョン番号を大きくします。たとえば、3.0.0 から 4.0.0 に変更します。 |
| CIAO_MVERSION_BUMP_MINOR | マイナーバージョン番号を大きくします。たとえば、4.1.0 から 4.2.0 に変更します。 |
| CIAO_MVERSION_BUMP_POINT | ポイントバージョン番号を大きくします。たとえば、5.2.3 から 5.2.4 に変更します。 |

## フラグ
| フラグ | 説明 |
| --- | --- |
| CIAO_COMMENT_PROMPT | コメント入力のプロンプトを表示します。 |
| CIAO_MVERSION_SILENT | ステータスバーを非表示にします。 |
| CIAO_MVERSION_PROMPT | [バージョン作成] ダイアログボックスを表示します。 |
| CIAO_MVERSION_DATA | バージョンデータベースに文書を含めます。 |
| CIAO_MVERSION_ACL | バージョンデータベースに ACL を含めます。 |
| CIAO_MVERSION_REPID | バージョンデータベースにレプリカ ID を含めます。 |
| CIAO_MVERSION_ODS_NOTES5 | バージョンデータベースの ODS を R5.x に変更します (R4.x はサポートされません )。 |
| CIAO_MVERSION_ODS_NOTES4 | バージョンデータベースの ODS を R4.x に変更します。 |
| CIAO_MVERSION_SAVE_ZIPPED | バージョンデータベースを ZIP ファイルとして保存します。 |
| CIAO_MVERSION_DEFAULT | ステータスバーを非表示にします。バージョンデータベースを ZIP ファイルとして保存します。 |
| CIAO_MVERSION_UI_SHOW_STATUS | ノーツステータスバーにバージョン操作の進行状況を表示します。 |
| CIAO_MVERSION_UI_SHOW_PROGRESS | プログレスバーを表示します。 |
| CIAO_MVERSION_NO_UI | UI を表示しません。すべてのオプションを CIAOMakeVersionImp 呼び出しに渡す必要があります。 |
| CIAO_MVERSION_FULL_UI | [バージョン作成] ウィンドウのすべてのオ プションを有効にします。これを指定しな い場合、バージョン番号フィールドは無効 になります。 |

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
status = CIAOMakeVersionImp( strPath, "BASELINE", "Initial baseline version", CIAO_MVERSION_DEFAULT )
If status <> 0 Then
    Dim szBuffer As String*255
    CIAOStringLoad status, szBuffer, 255
    MessageBox Left$( szBuffer, Instr( szBuffer, Chr(0) ) - 1 )
End If
```