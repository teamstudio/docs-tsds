# DIFFReportW32

## 説明
DIFFReportW32 と DIFFDataReportW32 とで 2 つのデータベースの設計要素あるいは文書を比較し、レポートを生成します

## シンタックス
### DIFFReportW32
```
status = DIFFReportW32( <Left>, <Right>, <Report>, <Title>, <Template>, <Filter>, <Flags> )
```

### DIFFDataReportW32
```
status = DIFFDataReportW32( <Left>, <Right>, <Report>, <Title>, <View>, <Template>, <Filter>, <Flags> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| Left | 入力 | String | 比較するいずれかのノーツデータベースのパス です。サーバー名とパス名は !! で区切ります。 |
| Right | 入力 | String | 比較するもう一方のノーツデータベースのパス です。サーバー名とパス名は !! で区切ります。 |
| Report | 入力 | String | 比較結果レポートの書き出し先ノーツデー タベースのパスです。サーバー名とパス名は !! で区切ります。 |
| Title | 入力 | String | レポートデータベースの新規作成時のタイトル です。 |
| View | 入力 | String | **DIFFDataReportW32 のみ**。 比較する文書の検索に使用するビューの名前で す。比較を行う両方のデータベースでこの ビューを使用する必要があります。 |
| Template | 入力 | String | レポートデータベースに使用されるノーツテンプレートのパスです。デフォルトのテンプレート (**tmslogs.ntf**) を使用するには、この部分を空白にするか、テンプレートファイルの場所を渡します。 |
| Filter | 入力 | String | 現在使用されていません。これは、"" とする必要があります。 |
| Flags | 入力 | Long | 任意の DBDIFF_FLAG_xxx 定数を渡すことができます。また、あらゆるフラグを組み合わせて渡すこともできます。 |

## フラグ
| フラグ | 説明 |
| --- | --- |
| DBDIFF_FLAG_SILENT | UI フィードバックを禁止します。 |
| DBDIFF_FLAG_SINGLE | 返答文書を使わずに、1つの大きなレポート文 書を作成します。データベースが小さい場合のみに使用するようお勧めします。 |
| DBDIFF_FLAG_SMART_FILTER | スマートフィルタを使用します。 |
| DBDIFF_FLAG_HIDE_ID_OBJECT | 同一の項目を非表示にします。 |
| DBDIFF_FLAG_HIDE_PROP | プロパティを非表示にします。 |
| DBDIFF_FLAG_HIDE_ID_PROP | 同一のプロパティを非表示にします。 |
| DBDIFF_FLAG_DEFAULT | デフォルトのオプション。DBDIFF_FLAG_HIDE_PROP を除くすべて。 |

## 戻り値
| 戻り値 | 型 | 説明 |
| --- | --- | --- |
| status | Long | 0 は、エラーが発生しなかったことを示します。戻り値が 0 で ない場合は、 [DIFFStringLoadW32](scriptstringload.md)使用して、エラーコード に関連するエラーメッセージを取得してください。 |

## 例
### DIFFReportW32
```vbscript
status = DIFFReportW32(
    "db1.nsf",_
    "db2.nsf",_
    "report.nsf",_ 'レポートデータベース
    "Delta Report",_ 'レポートデータベースのタイトル
    "",_ 'レポートにデフォルトの tmslogs.ntf テンプレートを使用する
    "",_ '未使用。空白にしてください。
    DBDIFF_FLAG_SILENT + DBDIFF_FLAG_SMART_FILTER)
```

### DIFFDataReportW32
```vbscript
status = DIFFDataReportW32(
    "db1.nsf",_
    "db2.nsf",_
    "report.nsf",_ 'レポートデータベース
    "Delta Report",_ 'レポートデータベースのタイトル
    "vwSelect",_ 'Name比較する文書をビューを使用して選択する
    "",_ 'レポートにデフォルトの tmslogs.ntf テンプレートを使用する
    "",_ '未使用。空白にしてください。
    DBDIFF_FLAG_SILENT + DBDIFF_FLAG_SMART_FILTER)
```