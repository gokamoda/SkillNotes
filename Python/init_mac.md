# MacでPython

- [1. 前提](#1-前提)
- [2. pyenvのインストール](#2-pyenvのインストール)
- [3. pythonのインストール](#3-pythonのインストール)
- [4. コードを書く](#4-コードを書く)

## 1. 前提
- Homebrewがインストールされている

## 2. pyenvのインストール
```shell
$ brew install pyenv
$ echo 'eval "$(pyenv init --path)"' >> ~/.zprofile
$ echo 'eval "$(pyenv init -)"' >> ~/.zshrc
$ exec $SHELL
```

## 3. pythonのインストール
1. `$ pyenv install 3.8.8` などとpythonのバージョンを指定してインストール
2. `$ pyenv versions` でインストールされているpython環境一覧を表示
3. `$ pyenv global 3.8.8` などで使用する環境を指定する

## 4. コードを書く
- VSCodeで書く
- 詳しくは`/VSCode/pytnon.md`