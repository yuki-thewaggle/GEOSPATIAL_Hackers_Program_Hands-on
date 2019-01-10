---?color=#F39F39
# @css[headline](環境構築)

---
## インストールが必要なもの
1. firefox & RestClient
2. テキストエディタ
3. Elixir
4. node.js
5. PostgreSQL
6. Phoenixframework

---
## APIを叩くためのRest APIクライアントが必要

今回は、[Firefox](https://www.mozilla.org/ja/firefox/new/?utm_campaign=non-fx-button&utm_content=rta%3Ae2FkMGQ5MjVkLTg4ZjgtNDdmMS04NWVhLTg0NjM1NjllNzU2ZX0&utm_medium=referral&utm_source=addons.mozilla.org)「[RESTClient](https://addons.mozilla.org/ja/firefox/addon/restclient/)」を利用します。

ダウンロードしてインストールしください。
![Restclient](template/img/environment/RestClient-add.png)

---
## エディタのインストール

テキストエディタ、普段ご利用のものをお使いください。

入ってない方は、この講座では以下を利用しています。

[VSCODE](https://code.visualstudio.com/)<br/>

---
## アドインの追加
VSCODEにElixirのアドインを追加します。

[MarketplaceよりElixirのアドイン追加](https://marketplace.visualstudio.com/items?itemName=mjmcloug.vscode-elixir) 

![Elixirのアドイン追加](template/img/environment/vscode-elixir.png)

---
## ターミナルからエディタを起動するための準備
VSCODEを開いた状態で

Command + Shift + P で検索窓を開きます。

![vscodeのアドイン追加](template/img/environment/vscode-adin.png)

---

「Shell」を検索し、インストールします。

![vscodeでshellを検索](template/img/environment/vscode-shell.png)

---
## ターミナルとは

プログラミングをする際に、コマンドを用いて操作や設定などを行うためのツール

WindowsとMacで呼び名と使用するコマンドが若干異なる

* Windows->コマンドプロンプト
* Mac->ターミナル

---?color=#333333
## ターミナルの使い方（Mac）

@css[code](現在のディレクトリ内にあるファイルやディレクトリの確認)

```
ls
```
@css[code](任意のディレクトリに移動する方法)

```
cd  ディレクトリ名
```

@css[code](新規ディレクトリ作成)

```
mkdir 任意のディレクトリ名
```

---?color=#33333

## コマンドプロンプトの使い方（Windows）

@css[code](現在のディレクトリ内にあるファイルやディレクトリの確認)
```
dir
```

@css[code](任意のディレクトリに移動する方法)
```
cd ディレクトリ名
```

@css[code](新規ディレクトリ作成)
```
mkdir 任意のディレクトリ名
```

---
## ターミナルからエディタを起動する方法
cd コマンドを使用しプロジェクトで使用するディレクトリに移動します
```
cd ディレクトリ名
```

移動後に、下記のコマンドで起動します
```
code .
```

VSCODEが起動すればOK

---
## エディタをターミナルから開く方法

エディタを開き
Command + Shift + Pでコマンドパレット開く。
「Shell」を検索しインストール。

ターミナルから```codeで```起動できます。

---
## Elixirのインストール
今回は、Elixirという言語を利用しますので

お使いの環境に合わせて、インストールしてください。

[Elixirのインストール方法](https://elixir-lang.org/install.html)

elixirに必要なパッケージ類も一緒にインストールされます。

---
## Macの場合
homebrewを使用すると便利です。

[homebrewのインストール方法](https://brew.sh/index_ja)

![MacでElixirのインストール](template/img/environment/elixir-install-mac.png)

---
インストール後homebrewをアップデート
```
brew update
```
アップデート後、下記コマンドでElixirのインストール
```
brew install elixir
```
---
## Windowsの場合
![WindowsでElixirのインストール](template/img/environment/elixir-install-win.png)

[Elixirのインストール方法](https://elixir-lang.org/install.html)内 Windowsの「Download the installer」

よりインストール。

---
## Elixirとは

> Elixir (エリクサー) は並行処理の機能や関数型といった特徴を持つ、Erlangの仮想マシン (BEAM) 上で動作するコンピュータプログラミング言語である。

引用元 [Wiki](https://ja.wikipedia.org/wiki/Elixir_(%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B0%E8%A8%80%E8%AA%9E))

---
## node.jsのインストール

https://nodejs.org/en/download/


---
## PostgreSQLのインストール

DBにPostgreSQLを利用します。まだインストールされてない方は以下より

[インストーラーでインストール](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)<br/>

ご利用の環境に合わせてダウンロードください。<br/>
今回は、version 11.1 をダウンロードします。

* パスワードはpostgresを設定します。

---
## Phoenixframeworkのインストール

Webのフレームワークとして、Phoenixを利用

[Phoenix](https://hexdocs.pm/phoenix/installation.html)<br/>

---
* Windows->プロンプト
* Mac->ターミナル

より、以下を入力してください。

```
mix archive.install hex phx_new 1.4.0
```
Phoenixがインストールされます。

---
## Serverを立ち上げよう
まずプロジェクトを作成します
```
mix phx.new sample
```
sampleの部分がプロジェクト名になります。

```
Fetch and install dependencies? [Yn] 
```
上記がターミナルに表示されたら　yを入力しEnter。

---
## Serverを起動しよう！
作成したプロジェクトフォルダに移動します。
```
cd sample
```
プロジェクトフォルダに移動できたら
```
iex -S mix phx.server
```
上記コマンドを入力、serverを起動します。

---
serverを起動したら、
ブラウザで「`http://localhost:4000`」にアクセス。

Phoenixで作られたデフォルトのWebページが表示される事を確認しましょう。

無事に見られたら、成功です。

---



