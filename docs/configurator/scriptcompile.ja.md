# CONFYCompileAndSign

## 説明
Configurator を実行して、データベースのすべてのノートをリコンパイル し、再度署名します ( エージェントを実行しているユーザーの ID を使用 )。 ユーザー ID は、処理されたノートの署名に使用されます。

## シンタックス
```
status = CONFYCompileAndSign( <SourceDatabasePath>, <Flags> )
```

## パラメータ
| パラメータ | 入力/出力 | 型 | 説明 |
| --- | --- | --- | --- |
| SourceDatabasePath | 入力 | String | 処理するノーツデータベースのパス です。サーバー名とパス名は !! で区切ります。 |
| Flags | 入力 | Long | 下記の CONFY_COMPILE_SIGN_xxx フラグの組み合わせ |

## フラグ
| フラグ | 説明 |
| --- | --- |
| CONFY_COMPILE_SIGN_DEFAULT | デフォルトの動作では、未署名の設計ノートをすべてコンパイルします ( エー ジェントを含む )。 通常、これは Configurator で変更されたノートのみになります。 |
| CONFY_COMPILE_SIGN_ALLBUTAGENTS | エージェント以外のノートをすべて含みます。 |
| CONFY_COMPILE_SIGN_AGENTS | エージェントを含みます。<br>注記 : エージェントに署名すると、そ のエージェントをサーバーから実行す る際に問題が生じる可能性があります。クライアント / サーバーでのエージェン トの実行については、『ノーツアプリ ケーション開発リファレンス』を参照し てください。 |
| CONFY_COMPILE_SIGN_UNSIGNED | 未署名の設計ノート (通常は Configurator で変更されたノート ) のみを処理します。 |
| CONFY_RUN_SILENT | ステータスバーを非表示にします。 |

## 戻り値
| 戻り値 | 型 | 説明 |
| --- | --- | --- |
| status | Long | 0 は、エラーが発生しなかったことを示します。戻り値が 0 でない場合は、[CONFYStringLoad](scriptstringload.md)を使用して、エラーコードに関連するエラーメッセージを取得してください。 |

## 例
```vbscript
status = CONFYCompileAndSign(
    "myserver!!dbtorun.nsf",_
    "CONFY_COMPILE_SIGN_ALLBUTAGENTS + CONFY_COMPILE_SIGN_UNSIGNED)
```