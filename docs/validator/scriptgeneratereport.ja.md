# LINKGenerateReport

## 説明
LINKGenerateReport は、データベース内のすべての文書を検査し、レポートを作成します。

## シンタックス
```
status = LINKGenerateReport( <SourcePath>, <OutputPath>, <OutputTitle>, <Select>, <Flags> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| SourcePath | 入力 | String | 処理するノーツデータベースのパス。サーバー名とパス名は !! で区切ります。 |
| OutputPath | 入力 | String	| Validator レポートデータベースのパス。指定したデータベースが存在しない場合は、 Validator によって作成されます。サーバー名とパス名は !! で区切ります。 |
| OutputTitle | 入力 | String | レポートデータベースのタイトル。 データベースがすでに存在する場合は、使用されません。 |
| Select | 入力 | String	| データ文書の検索時に、選択式または ビューを指定するために使用します LINK_VERIFY_DOCUMENTS は、Flags の 1 つとして渡されます 。 LINK_VERIFY_DOCUMENTS フラグのみを指定する場合、このパラメータは、デー タベースでデータ文書を検索するのに使用 する選択式を表します。 LINK_VERIFY_DOCUMENTS_BYVIEW フラグも指定する場合は、このパラメータはデータ文書の検索に使用するビューを表します。 |
| Flags | 入力 | Long | 下記の LINK_xxx フラグは組み合わせて渡すこともできます。 |

## フラグ
| フラグ | 説明 |
| --- | --- |
| LINK_VERIFY_DOCUMENTS | Validator を文書上で実行します。 |
| LINK_VERIFY_DESIGN | Validator を設計ノート上で実行します。 |
| LINK_VERIFY_DOCUMENTS_BYVIEW | LINK_VERIFY_DOCUMENTS を指定した場合,  選択式ではなくビューを使用して文書を選択します。 |
| LINK_FLAG_REPORT_ALL | 正常なリンクを含め、すべてのリンクを報告 します。 |
| LINK_FLAG_NO_WARNINGS | 警告を報告しません。 |
| LINK_FLAG_NO_URLS | URL を確認しません。 |
| LINK_FLAG_NO_EXTERNAL_LINKS| 現在のデータベースを指定しないリンクを許可しません。 |
| LINK_FLAG_NO_REPL_LOCAL | ローカルでないレプリカを検索しません。 |
| LINK_FLAG_NO_FIELDS | フィールドを確認しません。 |
| LINK_FLAG_NO_EMPTY_FIELDS | 空のフィールドを無視します。 |
| LINK_FLAGS_DEFAULT | Validator のデフォルトを使用します ( バックグランドで、文書上で実行 )。 |
| LINK_RUN_SILENT | バックグランドで実行します。 |
| LINK_IGNORE_CONFLICTS | 保存または複製時の競合の有無を確認しません。 |

## 戻り値
| 戻り値 | 型 | 説明 |
| --- | --- | --- |
| status | Long | 0 は、エラーが発生しなかったことを示します。戻り値が 0 でない場合は、 [LINKStringLoad](scriptstringload.md)  を使用して、エラーコードに関連するエラーメッセージを取得してください。 |

## 例
``` vbscript
status = LINKGenerateReport(
    "myserver!!dbToRun.nsf",_
    "linkreport.nsf",_ 'レポートデータベースの指定
    "Validator Report",_ 'レポート使用するタイトル
    "@ALL",_ '文書の選択式
    LINK_FLAGS_DEFAULT)
```