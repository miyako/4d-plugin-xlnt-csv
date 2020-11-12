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
$dst:=System folder(Desktop)+"test"
convert xlsx to csv ($src;$sheets;$password;$dst)
```

* カンマ以外のフィールド区切りは``$5``で指定できます。

* ``CRLF``以外のフィールド区切りは``$6``で指定できます。

* 値のエスケープは特にしません。

* シート名＋拡張子``.csv``がファイル名になります。

* シートの配列を指定しなかった場合，すべてのシートが対象になります。

[miyako.github.io](https://miyako.github.io/2020/11/11/4d-plugin-xlsx-to-csv.html)
