# テンプレートのカスタマイズ

Analyzer をインストールすると、DEANTemplate というテンプレート名をもつ **ivesdean.ntf** という名前のデータベーステンプレートファイルが自動的に作成されます。このテンプレートは、Analyzer が分析結果データベースを作成する際に使用されます。このデータベースに、ノーツテンプレートやデータベース設計の分析文書が 1 つ以上保存されます。
 
!!! note
    ロータススクリプト、式コード、Java、および JavaScript は常にリッチテキ ストで記述されています。これは、通常のテキストフィールドの場合、ノー ツクライアントの容量の上限が 15 KB であるのに対し、コードの上限は 64 KB であるためです。ビューの選択式ではリッチテキストフィールドを参 照できないため、一見すると制約があるように思えるかもしれません。 @Abstract を実行するエージェントを作成すれば、リッチテキストを通常のテ キストに変換し、同時に容量を 15 KB 以下に納めることができます。たとえ ば、以下のようにします。 
    ```
    FIELD ScriptBegins :=
    @If(fflpScripts="";"";@Abstract([Save]:[Abbrev];14999;"";"fflpScript"))
    ```
 
テンプレートをカスタマイズして、追加のビューまたはノーツエージェン トを作成することもできます。

## カスタマイズ可能なテンプレートを作成するには
1. ノーツから、TeamstudioAnalyzerテンプレート(**ivesdean.ntf**)の新しいコピー を作成します。
2. 新しいファイルの[データベースプロパティ]ウィンドウを開きます。[設計] タブをクリックします。
3. [ 設計 ] タブで、新しいテンプレートの名前を変更します。
4. [ データベースカテゴリ ] ボックスに「DEANTemplate」と入力します。

新たに分析結果データベースを作成する場合は、作成済みのテンプレートの一覧からテンプレートを選択し、それに基づいて設計を作成します。

結果データベースのテンプレート内のフォームに、フィールドを追加でき ます。フィールドには、コメントなど、データベースに追加する情報を含 めることができます。この追加フィールドは、分析結果が更新されても上 書きされません。

!!! note
    設計ノートやフィールドの場合、ユーザーが定義したフィールドの内容が保 持されるのは、次回の Analyzer 実行時までです。
    
同様に、分析結果データベーステンプレートにフォームを追加して、キャ プチャしたい任意のデータを保持することもできます。これらのフォーム は、Analyzer で作成されたデータをフォームに抽出する式とスクリプトを 任意で使用して、作成したり編集したりできます。

!!! note
    分析結果が更新される際、ユーザーによって定義されたフォームは上書きさ れませんが、主要文書、および設計ノートやフィールドへの返答文書の場合、 ユーザーによって定義されたフォームから作成された文書が保持されるの は、次回の Analyzer 実行時までです。