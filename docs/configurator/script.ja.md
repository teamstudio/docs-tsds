# 紹介

ロータススクリプトを使用して、Configurator を起動することができます。 Teamstudio Reports テンプレート (**tmslogs.ntf**) に付属している Configurator スクリプトライブラリを使用すると、検索および置換の設定をバッチ処理で実行するようセットアップできます。

この項では、Configurator スクリプトライブラリの各関数について詳しく説明します。その後、エージェントでスクリプトライブラリを使用する方 法を紹介します。

Configurator スクリプトライブラリには、次の関数が用意されています。

| Function | Description |
| --- | --- |
| [CONFYFindAndReplace](scriptfar.md) | 指定のデータベースで検索と置換を実行します。検索の際にデフォルト値を推定し、その結果を tmslogs.ntf から作成されたデータベースに出力し ます。検索と置換の件数を返します。 |
| [CONFYFindAndReplaceEx](scriptfar.md) | 選択式を使用することにより、検索する設計要素を指定できます。検索の際にデフォルト値を推定し、その結果を tmslogs.ntf から作成されたデータベースに出力します。検索と置換の件数を返します。 |
| [CONFYFindAndReplaceEx2](scriptfar.md) | 式を渡すことにより、検索する設計要素を指定できます。ログデータベースと文書タイトルも指定できます。検索の際にデフォルト値を推定し、その結果を tmslogs.ntf から作成されたデータベースに出力します。検索と置換の件数を返します。 |
| [CONFYCompileAndSign](scriptcompile.md) | Configurator を実行して、データベースのノートをリコンパイルし、再度署名します ( エージェントを実行しているユーザーの ID を使用 )。 |
| [CONFYStringLoad](scriptstringload.md) | FindAndReplace から返されたエラーメッセージを 取得します。 |