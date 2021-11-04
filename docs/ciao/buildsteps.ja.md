# 紹介

最も簡素なビルドパスは次の設定文書から構成されています。元になるテンプレート(またはデータベース)の定義、加えてターゲットとなるテンプレートの場所を示すプロモーションパス文書です。CIAO! ではプロモーションパス文書に以下の任意のステップを追加できる機能を提供しています:

* [Design Audit](bsaudit.md) – Teamstudio Anayzer をコールし、元になるテンプレートの設計に対してコーディング規約やルックアンドフィールの標準化などのチェックを行えます。
* [Make Version](bsversion.md) – Teamstudio CIAO! をコールし、設計テンプレートのバージョンを管理できます。
* [ACL Settings](bsacl.md) – プロモーションしたテンプレートに対する ACL と ACL エントリを設定できます。
* [Database Properties](bsdbproperties.md) – タイトル、カテゴリー、テンプレートからの継承、マスターテンプレート名の設定やそのクリアなどが行えます。またテンプレートのバージョン、名前、日付などバージョン情報をセットしたり、 $TemplateBuild 共有フィールドも編集可能です。
* [Copy Database](bscopy.md) – 元のテンプレートを別の場所にコピーを作成することができます。
* [Search and Replace](bssearch.md) – Teamstudio Configurator をコールし、ビルドの一部分として検索と置換を実行できます。ユーザーがバージョン番号や作成日付をアプリケーション内の設計要素で目視できる方法があげられます。
* [Compile LotusScript](bscompile.md) – ビルドの一部分としてプロモーションするテンプレート内のすべての LoutsScript をコンパイルしたり特定の LotusScript のある設計要素に対してのみコンパイルすることができます。
* [Element Properties](bselemproperties.md) – 設計の更新を禁止するフラグや禁止を通知するフラグ、設計の継承オプション、設計要素のコメントフィールドに対して編集を行うことができます。
* [Sign Database](bssign.md) – ビルドの一部分として特定の ID や格納 ID で設計(またはデータベース）に署名できます。
* [Refresh/Replace Design](bsrefresh.md) – プロモーションしたテンプレートをもとにターゲットのデータベース(群）に設計を更新することができます。
* [Email Notification](bsemail.md) – プロモーションおける結果をユーザーまたはグループにメール配信し通知するのに使用します。

これらのステップは Teamstudio Build Manager で利用できるビルドステップのサブセットです。Build Manager にはその他に複雑なビルドやリリースプロセスを管理する機能が提供されています。Build Manager に関する詳細の情報は[製品比較- CIAO! と Build Manager](promotioncompare.md)をご参照ください。