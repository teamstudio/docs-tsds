# DEANAnalyzeAndAudit

## 説明
Analyzer Audit を呼び出します。指定のデータベースで、分析および監査を実行します。

## シンタックス
``` 
status = DEANAnalyzeAndAudit( <Design>, <Analysis>, <Title>, <Template>, <AuditIn>, <AuditOut>, <AuditOutTitle>, <AuditClass>, <Filter>, <Flags> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
|Design | 入力 | String | 分析するデータベースのパス。サーバー名とパス名は !! で区切ります。 |
| Analysis | 入力 | String | 分析結果データベースのパス。サーバー名とパス名は !! で区切ります。 |
|Title | 入力 | String | The分析結果データベースのタイトル。 |
| Template | 入力 | String | 新規の分析結果データベースが作成される際に使用する分析テンプレートのパス。サーバー名とパス名は !! で区切ります。デフォルトのテンプレートを使用する場合は空白の文字列 "" を指定します。 |
| AuditIn | 入力 | String | 監査機能のフィルタデータベースのパス。 サーバー名とパス名は !! で区切ります。 |
| AuditOut | 入力 | String | 監査結果データベースのパス。サーバー名とパス名は !! で区切ります。 | 
| AuditOutTitle | 入力 | String | 監査結果データベースのタイトル。 |
| AuditClass | 入力 | String | 監査で使用するフィルタクラスの名前。 |
| Filter | 入力 | String | 分析対象となる設計要素をそれぞれ指定する[Analyzer 使用時のコンテキストフィルタ](scriptctxfilter.md)の文字列を指定します。すべての設計を分析する場合には空白も文字列 "" を指定します。 |
| Flags | 入力 | Long | このパラメータで Analyzer の動作を制御できます。制御には[DBDEAN の有効なフラグ](scriptflags.md)を渡します。フラグはプラス記号(+) を使用して組み合わせて渡すこともできます。 |

## 戻り値
| 戻り値 | 型 | 説明 |
| --- | --- | --- |
| status | Integer | 0 は、エラーが発生しなかったことを示します。戻り値が 0 で ない場合は、[DEANStringLoadW32](scriptstringload.md) を使用して、エラーコードに関するエラーメッセージを取得してください。 |

## 使用例
``` vbscript
status = DEANAnalyzeAndAudit(_
    "myserver!!dbtorun.nsf",_ '分析するデータベース
    "dbout.nsf",_ '分析結果データベース
    "Analysis of dbtorun",_ '分析結果データベースのタイトル
    "",_ 'デフォルトのテンプレートを使用する,
    "deanfltr.nsf",_ 'デフォルトのフィルタデータベース
    "dbAuditOut.nsf",_ 'database for audit results
    "Audit of dbtorun",_ '監査結果データベース
    "UI Standards",_ 'フィルタクラス
    "-FM",_ 'フォームだけを分析
    DBDEAN_FLAG_DEFAULT) 'status = DEANAnalyzeAndAudit(_
    "myserver!!dbtorun.nsf",_ '分析するデータベース
    "dbout.nsf",_ '分析結果データベース
    "Analysis of dbtorun",_ '分析結果データベースのタイトル
    "",_ 'デフォルトのテンプレートを使用する,
    "deanfltr.nsf",_ 'デフォルトのフィルタデータベース
    "dbAuditOut.nsf",_ '監査結果データベース
    "Audit of dbtorun",_ '監査結果データベースのタイトル
    "UI Standards",_ 'フィルタクラス
    "-FM",_ 'フォームだけを分析
    DBDEAN_FLAG_DEFAULT) '分析結果データベースが存在しない場合は新規作成する
```