# テンプレートとテンプレートにリンクする要素の使い方
設計要素がその設計をテンプレートから継承する場合、CIAO! のユーザー列にテンプレート名が表示されます。それらの要素をチェックアウトすることはできません。それらの要素を変更するには、ソーステンプレートで変更を加えます。

Tテンプレートにリンクする要素をチェックアウトできるようにするには、CIAO!設定データベースを開き、**[テンプレートにリンクする要素を監視しますか ?]** フィールドを **[ はい ]** に設定します。

* デフォルト設定の [ いいえ ] では、テンプレートにリンクする要素の監視は行 われません。この場合、ノーツによる通常テンプレートの再設計などの更新が ブロックされません。
* フィールドを [ はい ] に設定すると、設計要素のテンプレートへのリンクが無視されます。この場合、他の設計要素と同様、設計要素をチェックアウトしなければ更新がブロックされます。
