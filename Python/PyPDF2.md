# PyPDF2の利用

## Documentation
- https://pypdf2.readthedocs.io/en/latest/index.html

## Merge
```Python
from PyPDF2 import PdfMerger

merger = PdfMerger()
files =  ["doc.pdf", "doc.pdf"]

for pdf in files:
merger.append(pdf)

merger.write("output.pdf")
merger.close()
```

- mergeするファイルの引数はファイルパスを表すstr

## ディレクトリ内のファイルのパスをすべて取得する
```Python
import glob
files = glob.glob("src/*")
```