# WindowsでPython

## pyenvのインストール
- 参考：https://github.com/pyenv-win/pyenv-win

1. 管理者権限でPowerShellを起動
   ```shell
   $ Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
   $ Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"
   ```
2. 環境変数とパスの追加
    ```Shell
    $ [System.Environment]::SetEnvironmentVariable('PYENV',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
    $ [System.Environment]::SetEnvironmentVariable('PYENV_ROOT',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
    $ [System.Environment]::SetEnvironmentVariable('PYENV_HOME',$env:USERPROFILE + "\.pyenv\pyenv-win\","User")
    $ [System.Environment]::SetEnvironmentVariable('path', $env:USERPROFILE + "\.pyenv\pyenv-win\bin;" + $env:USERPROFILE + "\.pyenv\pyenv-win\shims;" + [System.Environment]::GetEnvironmentVariable('path', "User"),"User")
    ```
3. 再起動
4. `$ pyenv --version` を実行してインストールを確認

## pythonのインストール
1. `$ pyenv install 3.8.8` などとpythonのバージョンを指定してインストール
2. `$ pyenv versions` でインストールされているpython環境一覧を表示
3. `$ pyenv global 3.8.8` などで使用する環境を指定する

## コードを書く
- VSCodeで書く
- 詳しくは`../VSCode/pytnon.md`