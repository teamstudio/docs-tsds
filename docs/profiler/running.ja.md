# アプリケーション上での Profiler の実行

アプリケーションで Profiler を実行するには、対象となるデータベースを選択して Profiler 設定を設定し、アプリケーションを起動して Profiler を停止します。
 
!!! note
    ノーツクライアントのキャッシュ方法により、Profiler を実行する前にノーツクライアントを再起動する必要があります。 
    
## Teamstudio Profiler を起動するには
1. Designer で、プロファイルするアプリケーションを開きます。
2. ツールバーの[Profiler]ボタンをクリックします。  
   Teamstudio Profiler ウィンドウが開き、一番上のフィールドにデータベースの名前が表示されます。  
   ![Profiler Window](img/running.png)
   
!!! note
    非表示の設計を含むデータベースはプロファイルできません。エラーが表示されます。  
    ![Profiler Error](img/running2.png)  
    **[OK]** をクリックしてエラーを確認すると、[Teamstudio Profiler] ウィンドウが表示されます。[ 開始 ] ボタンが無効になります。

## Profiler のオプションの設定
Profiler オプションは、次の表に示すように設定できます。

| オプション | 説明 |
| --- | --- |
| 関数のプロファイリング | 関数のタイミング情報を収集します。このオプションを選択する場合、[ エントリポイント ] オプションも選択できます。|
| 行のプロファイリング | ロータススクリプトの行のタイミング情報を収集します。このオプションを選択すると、最も詳細な情報が得られます。 |
| エントリポイント | 関数のエントリポイントの情報を収集します。エントリポイントは、Initialize、Terminate、Click、Bind Events などの関数です。このオプションは最も簡潔であるため、開始すべき場所が分かります。このオプションは、[ 関数のプロファイリング ] オプションも選択した場合のみ選択できます。|

!!! note
    行のプロファイリングは、.lss ファイルに含まれるコードには使用できません。

## プロファイルを開始するには
1. Profiler ウィンドウから、[ 開始 ] をクリックして Profiler を起動します。
2. データベースを開き、プロファイルするコードを通常起動するようにして使用します。

!!! note
    Profiler の実行中に Designer で保存作業を行わないでください。予期しない結果が発生します。
    
## Profiler が収集した結果を表示するには
1. 終了したら、Profiler アイコンをクリックして Profiler を停止します。 
Teamstudio Profiler の結果ウィンドウが表示されます。  
   ![Profiler Results](img/running3.png)
