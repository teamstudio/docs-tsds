# 紹介

ロータススクリプトを使用して、Analyzer を起動することができます。 Teamstudio Reports テンプレート (**tmslogs.ntf**) に付属している Analyzer スクリプトライブラリを使用すると、分析をバッチ処理で実行するようにセットアップできます。

この項では、Analyzer スクリプトライブラリの各関数について詳しく説明します。その後、エージェントでスクリプトライブラリを使用する方法を紹介します。

Analyzer スクリプトライブラリには、次の関数が用意されています。

| 関数 | 説明 |
| --- | --- |
| [DEANAnalyzeW32](scriptanalyze.md) | Analyzer を呼び出します。ファイル名のデータとフラグのみを渡します。 |
| [DEANAnalyze2W32](scriptanalyze2.md) | Analyzer を呼び出します。分析結果データベースのタイトル、分析結果データベースファイルの作成時に使用されるテンプレート、および分析する設計要素のタイプを示すフラグを渡します。 |
| [DEANAnalyzeAndAudit](scriptanalyzeandaudit.md) | Analyzer Audit を呼び出します。指定のデータベースで、分析および監査を実行します。 |
| [DEANStringLoadW32](scriptstringload.md) | DEANAnalyzeW32 や DEANAnalyze2W32 が返すエラーコードに関連付けられているエラーメッセージを取得します。 |

Teamstudio Reports テンプレート (tmslogs.ntf) で作業している場合、 Analyzer スクリプトライブラリを作成する必要はありません。他のデータベースやテンプレートで作業する場合は、このスクリプトライブラリもコピーする必要があります。