# VSCodeでLaTeX (Cloud LaTeX)

- [1. 前提](#1-前提)
- [2. 拡張機能をインストール＋初期設定](#2-拡張機能をインストール初期設定)
- [3. 追加拡張機能のインストール＋初期設定](#3-追加拡張機能のインストール初期設定)
- [4. プロジェクトごとの設定](#4-プロジェクトごとの設定)
- [5. キーマッピング](#5-キーマッピング)

## 1. 前提
- `/VSCode/init.md`にしたがってvscodeを設定済み

## 2. 拡張機能をインストール＋初期設定
1. Cloud LaTeX をインストール  
   ```SHELL
   $ code --install-extension cloudlatex.cloudlatex
   ```
2. CloudLatexにログイン
3. マイページの右上のドロップダウンメニューからプラグイン連携を選択
4. パスワードを入力してトークンを生成
5. VSCodeでコマンドパレットを開く（Ctrl + Shift + P ( ⌘ + ⇧ + P ) ）
6. `Cloud LaTeX: Set account`を選択
7. メールアドレス、cliemt、access-tokenを入力

## 3. 追加拡張機能のインストール＋初期設定
1. LaTeX　Workshopをインストール
   ```SHELL
   $ code --install-extension james-yu.latex-workshop
   ```

## 4. プロジェクトごとの設定
1. VSCodeでディレクトリを開く
2.  コマンドパレットを開く
3. `Cloud LaTeX: Setting`を選択
4. Workspaceタブを選択する（Userではない）
5. 設定を行う
    1.  OutDirでPDFなどの出力ファイルを保存するディレクトリを設定（”out”など）
    2.  Project IDを入力
        - Project IDは、CloudLatexのプロジェクトのURLに含まれる６桁程度の数字
    3. Enabledにチェックを入れる
    4. サイドバーのCLタブの中にある"Reload"をクリック
6. ファイルエクスプローラーにファイルが現れる（必要に応じてVSCodeを開き直す）
7. `/.vscode/settings.json`を以下のように編集する
   ```JSON
   {
        "cloudlatex.projectId": 123456,
        "cloudlatex.outDir": "out",
        "cloudlatex.enabled": true,

        "latex-workshop.latex.autoBuild.run": "never",
        "latex-workshop.latex.outDir": "out",
        "[latex]":{
            "editor.formatOnSave": false
        }
    }
   ```

## 5. キーマッピング
- latexではバックスラッシュを多用する．
- macではバックスラッシュが打ちにくい
- Karabiner-Elementsを利用してキーマッピングをする
- 詳細は`/Karabiner-Elements/backslask.md`