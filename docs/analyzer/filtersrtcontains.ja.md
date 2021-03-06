# TMSRTContains

この関数は、指定したリッチテキストフィールドで、特定の値を検索します。
```
TMSRTContains( FieldName ; Flags; Value )
```

## パラメータ
| パラメータ | 意味 |
| --- | --- |
| **FieldName** | <p>このパラメータは、現在の Analyzer 文書 上にあるリッチテキストフィールドの名 前を指定します。</p><p><b>[適用設計要素]</b>が<b>[エージェント]</b>であ る場合、Analyzer テンプレートの <b>[ エー ジェント ]</b> フォーム上に存在するリッチ テキストフィールドだけが検索対象にな ります。</p><p>または</p><p>このパラメータを <b>Rich Text</b> に設定する と、文書上のすべてのリッチテキスト フィールドが検索対象になります。</p>
| **フラグ** | 次の数値により、TMSRTContains 関数の検索方法 を指定します。これらのフラグは、OR 演算子で結 合できます。 |
| **値** | 検索するテキストを指定します。引用符 で囲んで文字列を指定することも、引用 符なしでフィールド名を指定することも できます。フィールド名を指定すると、検 索する値がそのフィールドから取得され ます。したがって、指定するテキストは 通常のテキストでなければなりません。 |

## フラグ

| フラグ | 意味 |
| --- | --- |
| 0 | 通常 |
| 1 | 全単語の一致 |
| 2 | 大文字・小文字を区別 |
| 4 | 濁音・半濁音を区別 |
| 8 | ワイルドカード |
