# gitで差分ファイルを集めたい
## どうしてもデプロイを手動でしたいといけない時に、これでしのぐ（と事故は減りやすい）

例えば以下はmasterブランチの一つ前のコミット（やマージ）との差分があったファイルのみ集計したい時に使う

```
git archive master `git diff --name-only master HEAD~` -o archive.zip
```

削除ファイルや追加ファイルなど、特定のファイルでエラーが出る場合はフィルターをかけれる
```
git archive master `git diff --name-only master revision --diff-filter=ACMR` -o archive.zip
```

「A=追加、C=コピー、M=変更、R=リネーム」らしい