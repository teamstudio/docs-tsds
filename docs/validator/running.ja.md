# Validator の実行

Validator を実行するには、まずオプションおよびパラメータを設定し、次に分析結果データベースのサーバー名およびパスを指定します。

## Validator を実行するには
1. 次のValidatorオプションを設定します。  
   <table><tr><th>オプション</th><th>説明</th></tr>
     <tr><td>すべてのリンクを報告する</td><td>すべての文書リンクに関して正常、異常を報告するレポート文書が作成されます。このオプションを選択する と、<b>[ 警告なし ]</b> オプションと <b>[URL を無視する ]</b> オプションが無効になります。</td></tr>
     <tr><td>No警告なし</td><td>警告として分類されるエラーは報告されません。報告されないエラーには、リンクが指定されていないホットスポットなどが含まれます。</td></tr>
     <tr><td>URL を無視する</td><td>URL が無視されます。インターネットに接続していない場合は、URL は確認されません。</td></tr>
     <tr><td>外部リンクなし</td><td>このオプションを選択した場合、現在のデータベースを指していないリンクはエラーとして報告されます。</td></tr>
     <tr><td>レプリカをローカルとみ なす</td><td>このオプションを選択すると、外部サーバー上のレプリカデータベースは検索されません。</td></tr>
     <tr><td>フィールドを処理しない</td><td>フィールドエラーが処理されません。</td></tr>
     <tr><td>キーワードフィールドを処 理しない</td><td>キーワードフィールドが無視されます。</td></tr>
     <tr><td>空のフィールドを無視する</td><td>空のフィールド(文書上のデータがないフィールド)が無視されます。</td></tr>
     <tr><td>競合文書を無視する</td><td>競合文書が無視されます。</td></tr>
   </table>
2. Validator では、設計要素と文書、またはそのいずれかを報告するよう設定することができます。文書を報告するよう設定した場合は、*[ 式による選択 ]* または *[ ビューによる選択 ]* を指定する必要があります。
    -  *[ 式による選択 ]* を指定すると、デフォルトとして「@ALL」が表示されます。検索用の有効な選択式を入力できます。
    -  *[ ビューによる選択 ]* を指定すると、ドロップダウンリストに指定可能なビューが表示され、ソースデータベースのビューの 1 つを選択することができます。
3. レポートデータベース(分析結果)のサーバー名およびパスを入力します。
4. **[ 実行 ]** をクリックして、レポートデータベースを作成します。  
   Validator により、レポートデータベースが作成され、自動的にレポートデータ ベースが開きます。
   <div class="admonition">
   <p class="admonition-title">Note</p>
   <ul>
     <li>Validator の実行中に <b>CTRL+BREAK</b> キーを押すと、Validator を その時点で停止し、レポートデータベースを開くことができます。</li>
     <li>出力データベースが存在しない場合、<b>[ ログデータベースの新 規作成 ]</b> ウィンドウが表示されて、新しいデータベースタイトルを入力できます。</li>
     </ul>
   </div>