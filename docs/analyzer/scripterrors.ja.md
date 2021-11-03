# エラーコード戻り値

Analyzer のいずれかの関数から返される可能性のある戻り値を次に示します。

| 値 | 意味 |
| --- | --- |
| NOERROR (0) | 操作が正常に完了しました。 |
| 0-65535 | ノーツ API のエラーコード。 |
| 65536 and above	| Teamstudio のエラーコード。 | 

| Teamstudio エラーコード値	| 意味 |
| --- | --- |
| IDERR_DEAN_BAD_CLASS (66816) | 既存の分析結果データベースのクラスは、 DEANTemplate ではありません。 |
| IDERR_DEAN_BAD_ANALYSIS (66817) | 分析結果データベースのロードビューが破損しています。無効な文書がデータベースに含まれています。 |
| IDERR_DEAN_DELETE_FAILED (66820) | Analyzer は、削除された設計ノートに対応する文書を削除できません。 |
| IDERR_DEAN_TEMPLATE_NOT_FOUND (66821) | 分析テンプレート (通常、**ivesdean.ntf**) が見つかりません。 |

!!! note
    返されるメッセージは他にも多数あります。エラーコードに関連づけられたメッセージを取得するには、 [DEANStringLoadW32](scriptstringload.md)関数を使用してください。