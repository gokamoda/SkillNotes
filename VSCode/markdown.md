# VSCodeでMarkdown
- [1. 前提](#1-前提)
- [2. 拡張機能をインストール](#2-拡張機能をインストール)
- [3. 目次（TOC）作成](#3-目次toc作成)

## 1. 前提
- `init.md`にしたがってvscodeを設定済み

## 2. 拡張機能をインストール
1. Markdown All in Oneをインストール
2. これにより、インデントやリスト、TOCの作成が簡単になる。
3. `code --install-extension yzhang.markdown-all-in-one` でも可
4. 拡張機能の設定を開く
5. `Markdown › Extension › Toc: Levels`を`2..6`に変更すると便利

## 3. 目次（TOC）作成
1. 目次を作成したい場所にカーソルを移動する
2. ⌘⇧P でコマンドパレットを開く
3. `Markdown All in One: Create Table of Contents`を選択
4. 見出し番号を振りたい場合は同じくコマンドパレットで`Markdown All in One: Add/Update ection numbers`を選択