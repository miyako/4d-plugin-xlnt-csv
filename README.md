# 4d-plugin-xlnt-csv
XLSXを単純にCSV変換する

**バージョン**: v14以上

#### つかいかた

XLSXドキュメントを開いてシート名の配列を取得する

```4d
C_TEXT($src)
ARRAY TEXT($sheets;0)
C_TEXT($password)

$src:=System folder(Desktop)+"test.xlsx"
get xlsx sheets ($src;$sheets;$password)
```

（つづき）シート名（複数指定可）のデータをCSVファイルに書き出す

```4d
$dst:=System folder(Desktop)+"sheet1.csv"
convert xlsx to csv ($src;$sheets;$password;$dst)
```
