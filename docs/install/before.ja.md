# インストールの前に

## システム要件の確認
Teamstudio クライアント製品は次のシステム要件が必要です:

* Windows 7, Windows 8, Windows 10, Windows 11 など Intel プラットフォーム上の Notes がサポートする Windows の各バージョン
  <div class="admonition note">
    <p class="admonition-title">Note</p>
    <p>Microsoft は すでに Windows XP と Windows Server 2003 のサポートを打ち切りました。Edition 33 以降はこれらのプラットフォームをサポートしていません。Windows XP および Windows Server 2003 上での弊社製品のご利用に関するご質問は弊社担当営業までお問い合わせください。</p>
  </div>
* HCLが現在サポートするNotesバージョン
  <div class="admonition note">
    <p class="admonition-title">Note</p>
    <P>Teamstudio Notes Toolsは、Notesの以前のバージョンでも動作し、テクニカルサポートもお客様に提供いたします。但し、HCLがサポートしていないNotesバージョン固有の問題に対しての修正をTeamstudioが提供できない場合がございます。その場合は、HCLがサポートしているNotesバージョンをご利用ください。</p>
    <p>以前のバージョンのNotesにTeamstudio NotesToolsをインストールする方法の詳細については、<a href="mailto:techsupport_japan@teamstudio.com">techsupport_japan@teamstudio.com</a>　にご連絡ください。</p>
    <p>HCL がサポートする Notes のバージョンを確認するには、次の HCL のサポートライフサイクルのサイトをご確認ください。<a href="https://www.hcl-software.com/jp/resources/product-release/search">https://www.hcl-software.com/jp/resources/product-release/search</a>(HCL英語サイトが開きます)</p>
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