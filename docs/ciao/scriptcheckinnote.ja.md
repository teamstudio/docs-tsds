# CIAODbCheckIn/OutNote2

## 説明
文書のチェックインまたはチェックアウト

## シンタックス
### CIAODbCheckOutNote2
```
status = CIAODbCheckOutNote2( <DatabaseHandle>, <NoteID>, <Comment>, <Flags> )
```

### CIAODbCheckInNote2
```
status = CIAODbCheckInNote2( <DatabaseHandle>, <NoteID>, <Comment>, <Flags> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| DatabaseHandle | 入力 | Long | NSFDbOpen へのロータススクリプトでラップしたコールを使用して、開いたデータベースのノートへアクセスするハンドル |
| NoteID | 入力 | Long	| The処理するノートの ID。NoteID プロパティから返った文字列値がある場合、次のようなコードを使って数値に変換することができます。 `noteID = Val("&H" & doc.NoteID & "&")` |
| Comment | 入力 | String | 操作で使用するコメント |
| Flags | 入力 | Long | 操作を制御するフラグ。0 または下記のフラグを組み合わせ使用し渡すことができます。複数のフラグはプラス記号 (+) を使って組み合わせることができます。 |

## フラグ
| フラグ | 説明 |
| --- | --- |
| CIAO_COMMENT_PROMPT | コメント入力のプロンプトを表示します。このオプションはコメント入力するための API 操作です。ロータススクリプト内の他の方法でもコメントを入力できる方法があるので、滅多に使用することはないと思われます。 |

## 戻り値
| 戻り値 | 型 | 説明 |
| --- | --- | --- |
| status | Long | 0 は、エラーが発生しなかったことを示します。戻り値が 0 で ない場合は、 [CIAOStringLoad](scriptstringload.md) を使用して、エラーコードに関連するエラーメッセージを取得してください。 |

## 例
```vbscript
Declare Function NSFDbOpen Lib "nnotes.dll" (Byval PathName As String, rethDB As Long) As Integer
Declare Function NSFDbClose Lib "nnotes.dll" (Byval hDB As Long) As Integer
  
hexNoteId = InputBox("Enter Note ID of design element to check out, as HEX", "NOTEID")
comment = InputBox("Enter a comment", "COMMENT")
flags = 0 'CIAO_COMMENT_PROMPT にフラグをセットしここでコメント入力をさせることもできますが、既に上でコメント入力ダイアログを別で表示しているのでここではフラグは不要にします
     
noteId = Val("&H" & hexNoteId & "&")
  
status = NSFDbOpen(db.server + "!!" + db.filePath, hdb)
If 0 <> status Then
    Error status
End If
  
status = CIAODbCheckOutNote2(hdb, noteId, comment, flags)
  
NSFDbClose(hdb)
```