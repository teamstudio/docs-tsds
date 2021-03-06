# はじめに：分析情報の表示

Analyzer では、カテゴリ別に設計要素情報を並べ替えて表示することができます。まず、ビューをどのような目的で使用し、どのようなアクションを取ればよいかを下の表に示します。

| 目的 | 分析出力データベースの表示内容 | 実行するアクション |
| --- | --- | --- |
| 設計要素が使用される 場所を確認する | 設計要素参照を表示 | <ol><li>左側のナビゲータを使用して対応する設計要素カテゴリを展開し、設計要素文書を開きます。参照が文書の 末尾に一覧表示されます。</li><li>[ 設計補助 ] ビューカテゴリに移動し、[ 従属要素 ] ビューを選択します。このビューには、設計要素カテゴリ別の従属要素と共にすべての設計要素が表示されます。</li></ol> |
| 最終更新日を確認する | すべての設計要素の最終更新日を表示 | [ 設計要素 ] カテゴリには、 最終更新日が表示される複数のビューがあります。 |
| デフォルトアクセスを確認する | データベースのアクセス制御リストを表示 | [ 分析 ] カテゴリには、ACL 分析のサブカテゴリがあります。 |
| ビューの列で一貫性を 確認する | ビューの列を表示 | [ 名前別オブジェクト ] カテゴリには、複数の設定(一 貫性のない場合が多い)が表示される、列と呼ばれるビューがあります。 |
| リファクタリングを必要とするサブルーチン を確認する | エージェントの行 とパラメータの数 を表示 | 設計カテゴリのコードの下 のスクリプトライブラリ は、コードの行数と宣言さ れた変数の数が一覧表示さ れる、Subs と呼ばれる ビューです。数が最も多い ものが最も複雑なサブルー チンであり、リファクタリ ングされている可能性があ ります。 |
| フィールドが参照され ている場所をすべて確 認する | [フィールドの相互参 照 ] フォルダを使用 | 任意のフィールド文書([ 名 前別オブジェクト ] カテゴ リのフォームの下)を、 [ フィールドの相互参照 ] フォルダにドラッグアンドドロップします。次に、[ 参 照の追加 ] ボタンをクリッ クします。そのフィールド を参照するすべての設計要 素がビューに含まれます。 |
