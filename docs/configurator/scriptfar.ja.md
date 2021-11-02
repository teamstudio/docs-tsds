# CONFYFindAndReplace

## 説明
3 種類 CONFYFindAndReplace 関数を使って、指定のデータベースで検索と置換を実行します。その結果を tmslogs.ntf から作成されたデータベースに出力し、検索と置換の件数を返します。Ex とEx2 の変数で操作に関するより多くのオプションを利用できます。

## シンタックス
### CONFYFindAndReplace
```
status = CONFYFindAndReplace( <SourceDb>, <LogDb>, <FindText>, <ReplaceText>,
    <MatchFlags>, <SearchFlags>, <RunFlags>, <SelectionString>, <FilterString>,
    <Searched>, <Found>, <Replaced> )
```
      
### CONFYFindAndReplaceEx
```
status = CONFYFindAndReplaceEx( <SourceDb>, <LogDb>, <FindText>, <ReplaceText>,
    <MatchFlags>, <SearchFlags>, <RunFlags>, <SelectionString>, <DesignSelectionString>,
    <FilterString>,   <Searched>, <Found>, <Replaced> )
```

### CONFYFindAndReplaceEx2
```
status = CONFYFindAndReplaceEx2( <SourceDb>, <LogDb>, <LogDbTitle>, <DocTitle>,
    <FindText>, <ReplaceText>, <MatchFlags>, <SearchFlags>, <RunFlags>,
    <SelectionString>, <DesignSelectionString>, <FilterString>,
    <Searched>, <Found>, <Replaced> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| SourceDb | 入力 | String | 検索するノーツデータベースのパスです。サーバー名とパス名は !! で区切ります。 |
| LogDb | 入力 | String | ログを書き込むログデータベースのパスです。サーバー名とパス名は !! で区切ります。このデータベースが存在しない場合は、Configurator によって作成さ れます。 |
| LogDbTitle | 入力 | String | **CONFYFindAndReplaceEx2 のみ有効。** ログデータベースのタイトルです。空白 ("") の場合、デフォルトの 'Confy Report' が使用されます。 |
| DocTitle | 入力 | String | **CONFYFindAndReplaceEx2 のみ有効。** ログ文書のタイトルです。空白 ("") の場合、デフォルトのタイトルである「Configurator レ ポート - 生成日 : < レポート作成日時 >、データベース <データベースタイトル (ファイル名)>」 が使用されます。 |
| FindText | 入力 | String | 検索対象のテキストです。 |
| ReplaceText | 入力 | String | 検索対象テキストを置換するテキストです。 |
| MatchFlags | 入力 | Long | このパラメータを使用して、一致条件を指定 します。スクリプ トライブラリで定義されている、いずれかの CONFY_MATCH_ xxx 定数を渡すことがで きます。また、あらゆるフラグをプラス記号(+)を組み合わせて渡すこともできます。 |
| SearchFlags | 入力 | Long | スクリプトライブ ラリで定義されている、いずれかの CONFY_SEARCH_xxx 定数を渡すことが できます。また、あらゆるフラグをプラス記号(+)を組み合わせて渡すこともできます。 |
| RunFlags | 入力 | Long | スクリプトライブラリで定義 されている、いずれかの CONFY_RUN_xxx 定数を渡すことができます。また、あらゆるフラグをプラス記号(+)を組み合わせて渡すこともできます。 |
| SelectionString | 入力 | String | データ文書を検索する際の選択式または ビューを指定するために使用します。<br>CONFY_SEARCH_DATA フラグのみを指 定する場合、このパラメータは、データベー スでデータ文書を検索するのに使用する選択式を表します。<br/>CONFY_SEARCH_BYVIEW フラグも指定する場合、このパラメータを使用して、データ文書の検索に使用するビューを指定します。 |
| DesignSelectionString | 入力 | String | **CONFYFindAndReplaceEx** and **CONFYFindAndReplaceEx2**  のみ有効. 設計要素の検索時に選択式を指定するのに使用します。検索フラグの 1 つ として CONFY_SEARCH_DESIGN を渡す必要があります。 |
| FilterString | 入力 | String | このパラメータを使用して、[ Analyzer 使用時のコンテキストフィルタ](../analyzer/scriptctxfilter.md)を指定します。ンテキストフィ ルタを使用すると、検索する設計要素のタイ プを指定できます。すべての設計ノートを検索するには空白文字 "" を使用します。 |
| Searched | 出力 | Long | 検索した設計 / 文書の数を返します。 |
| Found | 出力 | Long | 検索テキストが検出された回数を返します。 |
| Replaced | 出力 | Long | 検索テキストを置換した回数を返します。 |

## 一致フラグ
| フラグ | 説明 |
| --- | --- |
| CONFY_MATCH_DEFAULT | 次のいずれのフラグ ( オプション ) も設定されていません。 |
| CONFY_MATCH_WHOLEWORD | 全単語検索を有効にします。 |
| CONFY_MATCH_ACCENT | 濁点 / 半濁点の区別を有効にします。 |
| CONFY_MATCH_CASE | 大文字と小文字の区別を有効にします。 |
| CONFY_MATCH_WILDCARD | 検索文字列にワイルドカード文字を含めます。 |
| CONFY_MATCH_REGEXP | 検索文字列に正規表現を含めます。 |

## 検索フラグ
| フラグ | 説明 |
| --- | --- |
| CONFY_SEARCH_DEFAULT | デフォルトの動作では、設計の検索のみで、置換は実行しません。 |
| CONFY_SEARCH_DESIGN | データベースの設計要素を検索します。 |
| CONFY_SEARCH_DATA | 指定した選択式を用いてデータベースのデータ文書を検索します。 |
| CONFY_SEARCH_BYVIEW | CONFY_SEARCH_DATA を修正し選択式ではなくビュー上の文書を用いてデータ文書を検索します。 |
| CONFY_SEARCH_MODE_REPLACE | 実際に置換を実行します。このフラグを指定しないと、Configurator は検索のみを実行し置換は実行しません。 |

## 実行フラグ
| フラグ | 説明 |
| --- | --- |
| CONFY_RUN_DEFAULT | デフォルトの動作。Configurator は、ロータス スクリプトをリコンパイルせず、変更された項目をすべて再度署名します。 |
| CONFY_RUN_COMPILE | Configurator が変更した設計要素をすべてリコンパイルします。 |
| CONFY_RUN_NO_SIGN | ノートに再度署名しません。 |
| CONFY_RUN_SILENT | ステータスバーを非表示にします。 |
| CONFY_RUN_DOC_PER_NOTE | 検索する設計要素または文書ごとに、検索と置 換の詳細を含む単一のログ文書を生成します。 このフラグを使用しない場合、すべての情報が単一の文書に保存されるため、必要な情報を見つけにくくなる可能性があります。 |

!!! note
    複数の検索置換操作を実行する場合、コンパイルと署名を複数回行うのは非効率です。すべてに一度に署名することで、処理時間を短縮できます。 そのためには、CONFY_RUN_NO_SIGN フラグを指定し、 CONFY_RUN_COMPILE フラグを除外します。そのうえで、検索置換操作が完了した後に[CONFYCompileAndSign](scriptcompile.md関数を呼び出します。
    
## 戻り値
| 戻り値 | 型 | 説明 |
| --- | --- | --- |
| status | Long | 0 は、エラーが発生しなかったことを示します。戻り値が 0 で ない場合は、 [CONFYStringLoad](scriptstringload.md) を使用して、エラーコードに 関連するエラーメッセージを取得してください。 |

## 例
### CONFYFindAndReplace
```vbscript
status = CONFYFindAndReplace(_
    strSourceDatabase,_
    "confrep.nsf",_ '出力するログデータベース
    "Teamstudio",_ '検索対象のテキスト
    "TS",_ '置換後のテキスト
    CONFY_MATCH_DEFAULT,_ '一致フラグは使用しない
    CONFY_SEARCH_DESIGN + CONFY_SEARCH_MODE_REPLACE,_ '設計の検索と置換の実行
    CONFY_RUN_COMPILE,_ '変更した設計のリコンパイル
    "",_ 'Dataデータ文書選択式、使用しない
    "",_ 'コンテキストフィルタ、すべての設計要素タイプを含む
    numSearched,_ '検索した文書の数を受け取るパラメータ
    numFound,_ '検出回数を受け取るパラメータ
    numReplaced) '置換回数を受け取るパラメータ
```

### CONFYFindAndReplaceEx
```vbscript
status = CONFYFindAndReplaceEx(_
    strSourceDatabase,_
    "confrep.nsf",_ '出力するログデータベース
    "teamstudio",_ '検索対象のテキスト
    "Teamstudio",_ '置換後のテキスト
    CONFY_MATCH_CASE,_ '大文字小文字を区別する検索
    CONFY_SEARCH_DESIGN + CONFY_SEARCH_DATA + CONFY_SEARCH_MODE_REPLACE,_ '設計と文書データの検索および置換の実行
    CONFY_RUN_COMPILE,_ '変更した設計のリコンパイル
    "SELECT @All",_ '文書検索に使用される選択式
    |$Title="MainForm"|,_ '設計選択式、名前に MainForm ををもつもののみ検索
    "-FM",_ 'コンテキストフィルタ、フォームのみ検索
    numSearched,_ '検索した文書の数を受け取るパラメータ
    numFound,_ '検出回数を受け取るパラメータ
    numReplaced) '置換回数を受け取るパラメータ
```
    
### CONFYFindAndReplaceEx2
```vbscript
status = CONFYFindAndReplaceEx2(_
    "server!!dbToSearch.nsf",_ 'ソースデータベースサーバーとパス
    "confrep.nsf",_ '出力するログデータベース
    "Configurator Report",_ 'ログデータベースのタイトル（新規作成時）
    "Replace performed on server!!dbToSearch.nsf",_ 'ログ文書のタイトル
    "teamstudio",_ '検索対象のテキスト
    "Teamstudio",_ '置換後のテキスト
    CONFY_MATCH_CASE,_ 'Case sensitive search
    CONFY_SEARCH_DESIGN + CONFY_SEARCH_DATA + CONFY_SEARCH_MODE_REPLACE,_ '設計と文書データの検索および置換の実行
    CONFY_RUN_COMPILE,_ '変更した設計のリコンパイル
    "SELECT @All",_ '文書検索に使用される選択式
    |$Title="MainForm"|,_ '設計選択式、名前に MainForm ををもつもののみ検索
    "-FM",_ 'コンテキストフィルタ、フォームのみ検索
    numSearched,_ '検索した文書の数を受け取るパラメータ
    numFound,_ '検出回数を受け取るパラメータ
    numReplaced) '置換回数を受け取るパラメータ
```