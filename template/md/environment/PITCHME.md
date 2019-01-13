---?color=#F39F39
# @css[headline](環境構築)

---
@snap[midopoint north-west text-06]
### インストール
@snapend

1. firefox & RestClient
2. テキストエディタ
3. Elixir
4. node.js
5. PostgreSQL
6. Phoenixframework

---
@snap[north-west text-06]
### Rest APIクライアントの準備
@snapend

@snap[midopoint text-05]
今回は、[Firefox](https://www.mozilla.org/ja/firefox/new/?utm_campaign=non-fx-button&utm_content=rta%3Ae2FkMGQ5MjVkLTg4ZjgtNDdmMS04NWVhLTg0NjM1NjllNzU2ZX0&utm_medium=referral&utm_source=addons.mozilla.org)「[RESTClient](https://addons.mozilla.org/ja/firefox/addon/restclient/)」を利用します。

ダウンロードしてインストールしください。
@img[span-70](template/img/environment/RestClient-add.png)
@snapend
---
@snap[north-west text-06]
### エディタのインストール
@snapend

@snap[midopoint text-05]
テキストエディタ、普段ご利用のものをお使いください。<br>

入ってない方は、この講座では以下を利用しています。<br>

[VSCODE](https://code.visualstudio.com/)<br/>

@img[span-70](template/img/environment/vscode.png)

@snapend

---
@snap[north-west text-06]
### vscode-elixirの追加
@snapend

@snap[midopoint text-05]
VSCODEにElixirのアドインを追加します。

[MarketplaceよりElixirのアドイン追加](https://marketplace.visualstudio.com/items?itemName=mjmcloug.vscode-elixir) 

@img[span-70](template/img/environment/vscode-elixir.png)
@snapend

---
@snap[north-west text-06]
### ターミナルからエディタを起動するための準備
@snapend

@snap[midopoint text-05]
VSCODEを開いた状態で

Command + Shift + P で検索窓を開きます。

@img[span-70](template/img/environment/vscode-adin.png)
@snapend
---
@snap[north-west text-06]
### Shell Command install
@snapend

@snap[text-05]
「Shell Command: install 'code' command in PATH」を選択します。
@img[span-90](template/img/environment/vscode-shell.png)
@snapend

---
@snap[north-west text-06]
### ターミナル
@snapend

@snap[text-05]
ターミナルとは:コマンドベースの入力インターフェイス(略称：CUI）<br>
WindowsとMacでは利用するアプリ名と、利用するコマンドも若干異なります。<br>
* Windows->コマンドプロンプト
* Mac->ターミナル
@img[span-60](template/img/environment/terminal.png)
@snapend

---?color=#000000
@snap[north-west text-06 text-white]
### ターミナルの使い方
@snapend


@snap[midpoint text-06]

現在のディレクトリ内にある内容の確認

@gist[terminal](Yoosuke/ef45e8a06367c20cff7b4a46714fbd12)

@snapend

---?color=#000000

@snap[north-west text-06 text-white]
### ターミナルからエディタを起動する方法
@snapend

@snap[midpoint]
VSCODEが起動すればOK<br><br>

@gist[zoom-10](Yoosuke/6d2cfefcc23d71cf0911074a99787e88)

@[2](VScodeを立ち上げる)

@snapend


---
@snap[north-west text-06]
### Elixirのインストール
@snapend

@snap[text-05]
今回は、Elixirという言語を利用しますので

お使いの環境に合わせて、インストールしてください。<br>
elixirに必要なパッケージ類も一緒にインストールされます。

@img[span-60](template/img/environment/elixir-hp.png)<br>
[Elixir インストール](https://elixir-lang.org/install.html)

@snapend
---
@snap[north-west text-06]
### HomeBrewのインストール
@snapend

@snap[midpint text-07]
homebrewを使用すると便利です。<br>
@img[span-60](template/img/environment/elixir-install-mac.png)<br>
[homebrewのインストール方法](https://brew.sh/index_ja)

@snapend

---?color=#000000
@snap[north-west text-06]
### Elixirのインストール for Mac
@snapend

@snap[midpoint]

@gist[elixir zoom-10](Yoosuke/0abcd22f59dc8cc7c0db4509aa358253)


@[1](HomebrewのUpdateをします)
@[2](Elixirをインストールします)

@snapend
---
@snap[north-west text-06]
### Elixirのインストール for Windows
@snapend

@snap[midpoint text-06]
@img[span-90](template/img/environment/elixir-install-win.png)<br>

[Elixirのインストール方法](https://elixir-lang.org/install.html)<br>
 Windowsの「Download the installer」よりインストール。
@snapend
---
@snap[north-west text-06]
### node.jsのインストール
@snapend

@snap[text-05]
@img[span-70](template/img/environment/nodejs.png)<br>

[nodejs ダウンロード](https://nodejs.org/en/download/)
@snapend

---
@snap[north-west text-06]
### PostgreSQLのインストール
@snapend

@snap[text-05]
今回は、version 11.1 をダウンロードします。<br>
* パスワードはpostgresを設定します。<br>
[PostgreSQL インストール](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)<br>
@img[span-60](template/img/environment/postgresql.png)
@snapend
---
@snap[north-west text-06]
### Phoenixframeworkのインストール
@snapend

@snap[text-05]
Webのフレームワークとして、Phoenixを利用します<br>
[Phoenix](https://hexdocs.pm/phoenix/installation.html)<br/>
@img[span-70](template/img/environment/phoenix.png)

@snapend

---?color=#000000
@snap[north-west text-06 text-white]
### Phoenix v1.4のインストール
@snapend

@gist[elixir midpoint zoom-16](Yoosuke/02ec19b92d74e666fd6e47e7095dfd9c)

@snap[south text-04]
ターミナルからコマンドを入力してインストールします。
@snapend

---?color=#000000
@snap[north-west text-06 text-white]
### Phoenix プロジェクトの作成
@snapend

@snap[midpoint]
@gist[zoom-06](Yoosuke/a3b22fb6c27ef03d978d37bc80e88618)

@[1](gismapという名前でプロジェクトを作成します)
@[3](Yを入力します)
@[7](gismapのディレクトリに移動します)
@[11](DBを作成します)
@[15](サーバーを起動します)

@snapend
---
@snap[north-west text-06]
### WebServerの確認
@snapend

@snap[text-05]
ブラウザで「`http://localhost:4000`」にアクセス。<br>
Phoenixで作られたデフォルトのWebページが表示される事を確認しましょう。<br>
無事に見られたら、成功です。<br>

@img[span-60](template/img/environment/localhost4000.png)

@snapend



