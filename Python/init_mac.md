# MacでPython

## 前提
- Homebrewがインストールされている

## pyenvのインストール
```shell
$ brew install pyenv
$ echo 'eval "$(pyenv init --path)"' >> ~/.zprofile
$ echo 'eval "$(pyenv init -)"' >> ~/.zshrc
$ exec $SHELL
```

## pythonのインストール
1. `$ pyenv install 3.8.8` などとpythonのバージョンを指定してインストール
2. `$ pyenv versions` でインストールされているpython環境一覧を表示
3. `$ pyenv global 3.8.8` などで使用する環境を指定する

## コードを書く
- VSCodeで書く
- 詳しくは`../VSCode/pytnon.md`