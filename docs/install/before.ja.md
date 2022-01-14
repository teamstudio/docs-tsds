# インストールの前に

## システム要件の確認
Teamstudio クライアント製品は次のシステム要件が必要です:

* Windows 7, Windows 8, Windows 10, Windows 11 など Intel プラットフォーム上の Notes がサポートする Windows の各バージョン
  <div class="admonition note">
    <p class="admonition-title">Note</p>
    <p>Microsoft は すでに Windows XP と Windows Server 2003 のサポートを打ち切りました。Edition 33 以降はこれらのプラットフォームをサポートしていません。Windows XP および Windows Server 2003 上での弊社製品のご利用に関するご質問は弊社担当営業までお問い合わせください。</p>
  </div>
* HCLが現在サポートするNotes 9.0.x 以上のバージョン
  <div class="admonition note">
    <p class="admonition-title">Note</p>
    <p>Teamstudio Notes Tools typically work without issue on earlier versions of Notes, and technical support is available for customers on legacy versions of Notes. Teamstudio may not, however, be able to provide fixes for issues that are specific to unsupported versions of Notes. For more information on installing Teamstudio tools on earlier versions of Notes, contact <a href="mailto:techsupport@teamstudio.com">techsupport@teamstudio.com</a>.</p>
    <p>HCL がサポートする Notes のバージョンを確認するには、次の HCL のサポートライフサイクルのサイトをご確認ください。<a href="https://support.hcltechsw.com/csm?id=kb_article&sysparm_article=KB0068850&sys_kb_id=d9e7f06e1be51cd0f37655352a4bcb4d">https://support.hcltechsw.com/csm?id=kb_article&sysparm_article=KB0068850&sys_kb_id=d9e7f06e1be51cd0f37655352a4bcb4d</a>(HCL英語サイトが開きます)</p>
  </div>
* 約 50 MB のハードディスク空き容量
* HCL Notes が動作する充分な RAM
* ローカル PC にソフトウェアをインストールできる充分な Windows 上の権限

Teamstudio CIAO! Server は次のシステム要件が必要です:

* Domino サーバーが動作サポートする Windows サーバーの各バージョン
* HCL が現在サポートする 32bit と 64bit の Domino サーバーの各バージョン

Teamstudio Profiler Server は次のシステム要件が必要です:

* Domino サーバーが動作サポートする Windows サーバーの各バージョン
* HCL が現在サポートする 32bit の Domino サーバーの各バージョン


!!! Note
    このリリースに実装されている Analyzer Filters データベースは **deanfltr.ntf** です。
    
    以前のリリースで **deanfltr.ntf** を使用して、このテンプレートに何か変更を加えてある場合には、インストール前に他の名前に変えてバックアップしてください。そうしないと、これまでの変更やカスタマイズが失われることになります。
    
    フィルタデータベースをアップグレードするには:
    
    1. 現在の Analyzer フィルタデータベース (**deanfltr.nsf** あるいは **deanfltr.ntf**) のコピーを作成します。
    2. データベースを新規に作成します (**ファイル > データベース > 新規**) 、そしてファイル名を **deanfltr.nsf** とします。次にテンプレート指定のボックスから  Teamstudio Analyzer Filter Db を指定します。
    3. 既存のものに置き換えるかのプロンプトが出たら「はい」をクリックしてください。 (バックアップを取ってあるので大丈夫です。)
    4. これまでのカスタムフィルターを全部、この新しいデータベースにコピーしてください。