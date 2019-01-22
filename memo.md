# 構成

---

# Windowsメモ

### Phoenix v1.4 のインストール
- 管理者権限でコマンドプロンプトを起動する
- 入力するコマンドは同じ `mix archive.install hex phx_new 1.4.0`
```
C:\WINDOWS\system32>mix archive.install hex phx_new 1.4.0
Could not find Hex, which is needed to build dependency :phx_new
Shall I install Hex? (if running non-interactively, use "mix local.hex --force") [Yn] Y
* creating c:/Users/yukim/.mix/archives/hex-0.19.0
Resolving Hex dependencies...
Dependency resolution completed:
New:
[32m  phx_new 1.4.0[0m
* Getting phx_new (Hex package)
All dependencies are up to date
Compiling 10 files (.ex)
Generated phx_new app
Generated archive "phx_new-1.4.0.ez" with MIX_ENV=prod
Are you sure you want to install "phx_new-1.4.0.ez"? [Yn] Y
* creating c:/Users/yukim/.mix/archives/phx_new-1.4.0
```
---

### Visual Studio Code の使い方
- 管理者権限で Visual Studio Code を起動する
- 入力するコマンドを `code .` から `code . -r` に変える
