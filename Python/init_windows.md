# windowsでPython

## pyenvのインストール
- 参考：https://github.com/pyenv-win/pyenv-win

1. 管理者権限でPowerShellを起動
2. `$ Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine` を実行
3. `Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"` を実行
4. 再起動
5. `pyenv --version` を実行してインストールを確認

## pythonのインストール
1. `pyenv install 3.8.8` などとpythonのバージョンを指定してインストール
2. `pyenv versions` でインストールされているpython環境一覧を表示
3. `pyenv global 3.8.8` などで使用する環境を指定する

## コードを書く
- VSCodeで書く
- 詳しくは`../VSCode/pytnon.md`