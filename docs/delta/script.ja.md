# 紹介

ロータススクリプトを使用して Delta を起動することができます。Delta (**tmslogs.ntf**) に含まれる Delta スクリプトライブラリを使用して、2 つの データベースの比較をバッチ処理するように設定できます。

この項では、Delta スクリプトライブラリの各関数について詳しく説明します。その後、エージェントでスクリプトライブラリを使用する方法を紹介 します。

Delta スクリプトライブラリには、次の関数が用意されています。

| 関数 | 説明 |
| --- | --- |
| [DIFFReportW32](scriptreport.md) | 2 つのデータベースの設計要素を比較し、レポートを 生成します (1 つのデータベースをそのデータベー ス自体と比較することもできます )。 |
| [DIFFDataReportW32](scriptreport.md) | 2 つのデータベースの文書を比較します。 |
| [DIFFStringLoadW32](scriptstringload.md) | API から返されたエラーコードに関連付けられているエラーメッセージを取得します。 |