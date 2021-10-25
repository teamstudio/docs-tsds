# Profiler Server の使用

ドミノサーバーで Profiler Server をインストールすると、スケジュールされたエージェントや Web エージェントの実行パフォーマンスを監視できます。

Profiler Server は、サーバーで次のデータベースを使用します。

* Teamstudio/ProfilerConfig.nsf – 監視対象を Profiler に指定します。
* Teamstudio/ProfilerLog.nsf – Profiler の結果が保持されます。 
 
!!! note
    Profiler は、エージェントを常時監視するようには設計されていません。エージェントが Profiler を起動するたびに、パフォーマンスはかなり低下します。Profiler を使用しないときは、Profiler 設定データベース内のすべてのエージェントを無効にしておくことをお勧めします。