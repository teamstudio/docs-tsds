# コールツリーの使用

コールツリーを使って結果を調査することもできます。コールツリーには、Profiler の実行中にコールされた関数がさまざまな方法で表示されます。

## コールツリーを使うには
1. **[ 表示 ] > [ コールツリー ]** をクリックします。**[ コール ]** ウィンドウが表示されます。
2. 関数を選択し、**[関数を表示]**ボタンをクリックすると、メイン結果ペイン内か ら自動的にその関数が強調表示されます。  
   ![Call Tree](img/calltree.png)
3. **[ 子関数を結合する ]** チェックボックスをオンにすると、似ているコールが 1 つ のエントリとして **[ コール ]** ウィンドウに表示されます。  
   この機能を使うと、ツリーをシンプルにすることができます。たとえば、ある関数を数百回もコールするループがあったとしても、その関数はコールツリー に一度しか表示されません。チェックボックスをオフにすると、複製を含むすべての関数がツリーに表示されます
4. 調査が完了したら、**[閉じる]**をクリックします。  
   ファイルを保存するかどうかを確認するメッセージが表示されます。保存場所を指定すると、Profiler スナップショット(.tps ファイル)として保存されます。  
   **[ ファイル ] > [ 名前を付けて保存 ]** をクリックしてレポートを保存することも できます。