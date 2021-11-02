# Configurator エラーコード戻り値

戻り値の例を次に示します。

| 値 | 意味 |
| --- | --- |
| NOERROR (0) | 操作が正常に完了しました。 |
| 0-65535 | ノーツ API のエラコード。 |
| 65536 and above | Teamstudio のエラーコード。 |

| Teamstudio エラーコード値 | 意味 |
| --- | --- |
| IDERR_STAR_BAD_SELECTION_FORMULA (67585) | The指定した選択式が無効です。 |
| IDERR_STAR_BAD_SOURCE_DB (67586) | ソースデータベース名が無効です。 |
| IDERR_STAR_BAD_FIND_STRING (67587) | 検索文字列が無効です。 (例 有効な正規表現ではないなど) |

!!! note
    返されるエラーコードは他にも多数あります。エラーコードに関連付けられ たメッセージを取得するには、[CONFYStringLoad](scriptstringload.md)関数を使用してください。