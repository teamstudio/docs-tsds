# サーバーモジュールのインストール

必要に応じて、CIAO! および Profiler のサーバー版を Domino サーバーへインストールできます。

| サーバーツール | インストールの理由 |
| --- | --- |
| CIAO! Server | 追加の機能が使用できます。例えば、テンプレートがサーバー上にあり、設計要素をチェックアウトした時点で他の開発者からの修正から設計を保護することが可能です。 |
| Profiler Server | スケジュールエージェントと Web エージェントのパフォーマンスアクティビティをテストできます。 |

## Windows でのインストール手順

インストール前に次の事項をご確認ください:

* インストールするサーバーにひとつずつライセンスを購入する必要があります。CIAO! と Profiler のサーバー版は Domino サーバー毎にライセンスが必要です。

### CIAO! サーバー版のインストール

1. 以下のファイルをコピーします:
    1. nhkciao.dll と nhkciao.sym (32-bit のみ) ファイルをサーバーの実行ディレクトリーにコピーします (nserver.exe が存在するフォルダ)
    2. ciaologf.ntf と ciao.ntf をデータディレクトリーにコピーします。
2. Notes クライアントからサーバー上にあるテンプレートを使用してサーバー上に次のデータベースを作成します。  
    * CIAO\CIAOConfig.nsf (Template: Teamstudio CIAO! Configuration)  
    * CIAO\CIAOLog.nsf (Template: Teamstudio CIAO! Log File)
3. シリアルキー情報の追加:  
    1. teamstudio.ini というテキストファイルを Domino のデータディレクトリーに作成します。  
    2. 次の行を追加します:
    ```
    [CIAO]  
    HKCIAOKey=xxxxx-xxxxx-xxxxx,xx-xxxxx  
    CIAOConfigDb=CIAO\CIAOConfig.nsf  
    ```
   xxx の部分はお客様がお持ちのライセンスのシリアルキーに置き換えてください。
4. notes.ini に次の行を追加、既にある場合には修正をしてください:
```
NSF_HOOKS=hkciao
```
5. Domino サーバーを再起動します。  
   次のような行がコンソールに表示されれば正常にインストールが完了です:
```   
CIAO Server Hook started - (SERVER). (HKCIAO Edition 33 build xxxxx)
CIAO Server Hook: Using Configuration File: CIAO\CIAOConfig.nsf
```

### Profiler サーバー版のインストール
1. 以下のファイルをコピーします:
    1. nhkprofile.dll と nhkprofile.sym ファイルをサーバーの実行ディレクトリーにコピーします (nserver.exe が存在するフォルダ)
    2. profile.ntf と tmslogs.ntf をデータディレクトリーにコピーします。
2. Notes クライアントからサーバー上にあるテンプレートを使用してサーバー上に次のデータベースを作成します。
    * Teamstudio\ProfilerConfig.nsf (テンプレート: Teamstudio Profiler Configuration)
3. シリアルキー情報の追加:
    1. teamstudio.ini というテキストファイルを Domino のデータディレクトリーに作成します。
    2. 次の行を追加します:
    ```
    [Profiler]
    HKPROFKey=xxxxx-xxxxx-xxxxx,xx-xxxxx
    ProfilerServerConfig=Teamstudio\ProfilerConfig.nsf
    ```
    xxx の部分はお客様がお持ちのライセンスのシリアルキーに置き換えてください。
4. notes.ini に次の行を追加、既にある場合には修正をしてください:
```
NSF_HOOKS=hkprofile
```
5. Domino サーバーを再起動します。  
   次のような行がコンソールに表示されれば正常にインストールが完了です:
```
(namgr) - Profiler Server Hook started. (HKPROFILE Edition 33 build xxxxx)
Profiler Server Hook: Using Configuration File: Teamstudio\ProfilerConfig.nsf
```