# トラブルシューティング
通常よくある問題とその解決方法を以下のテーブルよりご確認頂けます。

| 問題/エラー | 対処法 |
| --- | --- |
| If you try to add or remove Teamstudio tools with Notes running, you may see a message that files are in use. If you choose to terminate Notes, you may get a message that the installer is unable to terminate Notes. | You can safely ignore this message which is coming from Windows Installer. You will be prompted later in the install to shut down Notes and this second attempt will be successful. |
| After installing Profiler, you see an error that NNOTES.dll cannot be found when you try to open a .tps file. | This problem can occur because nprofile.exe, the file that opens .tps files, is no longer in the Notes program directory and thus can no longer locate the Notes dlls it needs. To fix the error, add the Notes program directory to your Windows path. |

