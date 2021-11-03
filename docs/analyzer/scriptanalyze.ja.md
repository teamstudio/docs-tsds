# DEANAnalyzeW32

## 説明
Analyzer を呼び出します。ファイル名のデータとフラグのみを渡します。

## シンタックス
```
status = DEANAnalyzeW32( <Design>, <Analysis>, <Flags> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
|Design | 入力 | String | 分析するデータベースのパス。サーバー名とパス名は !! で区切ります。|
| Analysis | 入力 | String | 分析結果データベースのパス。サーバー名とパス名は !! で区切ります。 |
| Flags | 入力 | Long | このパラメータを使用すると、Analyzer の動作方 法を制御できます。Analyzer スクリプトライブラリで定義した、任意の[DBDEAN の有効なフラグ](scriptflags.md). を渡すことができます。フラグはプラス記号 (+) を使用して組み合わせて渡すこともできます。 |

## 戻り値
| 戻り値 | 型 | 説明 |
| --- | --- | --- |
| status | Integer | 0 は、エラーが発生しなかったことを示します。戻り値が 0 で ない場合は、[DEANStringLoadW32](scriptstringload.md)を使用して、エラーコードに関連するエラーメッセージを取得してください。 |

## 使用例
``` vbscript
status = DEANAnalyzeW32(_
    "myserver!!dbtorun.nsf",_ '分析するデータベース
    "dbout.nsf",_ '分析結果データベース
    DBDEAN_FLAG_SILENT + _ 'UI フィードバックなし
    DBDEAN_FLAG_NO_CREATE) '新規分析結果データベースを作成しない
```