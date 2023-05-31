# TMSGetParentValue

この関数は、Analyzer データベースに含まれる親文書からフィールド値を取得します。

```
TMSGetParentValue( <Form Alias>::<field name> )
```

## パラメータ
| パラメータ | 意味 |
| --- | --- |
| **&lt;Form Alias&gt;** | <p>このパラメータは、Analyzer の出力構造に基づいて、現在の文書の親 を指定している必要があります。</p><p>たとえば、フィールドは、フォームの親文書にはなれません。ただし、 フォームはフィールドの親になれます。また、設計要素の親には、データベース(CDBP00)のみを指定できます。</p> |
| **&lt;field name&gt;** | このパラメータには、ターゲット文書で有効なテキストフィールドを 指定する必要があります。有効なテキストフィールドが指定されてい ないと、この関数は失敗します。フィールドに、リッチテキストフィー ルドを指定することはできません。フィールドがテキストフィールド でない場合は、値がテキストに変換されます。 |

次に式の例を示します。
``` vbscript
TMSGetParentValue( CDBP00::fdbpFile )
```
この式は、現在のデータベースのファイル名を返します。

次のように TMSRTContains 式に組み込むこともできます。
```vbscript
TMSRTContains( Rich Text ; 0; TMSGetParentValue( CDBP00::fdbpFile ))
```
フィルタをチェックすると、まず **GetParentValue** が評価され、その戻り値が式に代入されます。次いで、式の残りが評価されます。この関数は、デー タベースを除くすべての **[ 適用設定要素 ]** フィルタで動作します。データベース文書には親がないためです。