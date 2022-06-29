# PyPDF2の利用
- [1. Documentation](#1-documentation)
- [2. Merge](#2-merge)
  - [2.1. ディレクトリ内のファイルのパスをすべて取得する](#21-ディレクトリ内のファイルのパスをすべて取得する)
## 1. Documentation
- https://pypdf2.readthedocs.io/en/latest/index.html

## 2. Merge
```Python
from PyPDF2 import PdfMerger

merger = PdfMerger()
files =  ["doc1.pdf", "doc2.pdf"]

for pdf in files:
    merger.append(pdf)

merger.write("output.pdf")
merger.close()
```

- mergeするファイルの引数はファイルパスを表すstr

### 2.1. ディレクトリ内のファイルのパスをすべて取得する
```Python
import glob
files = glob.glob("src/*")
```