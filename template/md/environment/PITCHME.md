---?color=#F39F39
# @css[headline](環境構築)

---
@snap[midopoint north-west text-06]
### 準備するもの
@snapend

1. Rest APIクライアント
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
今回は、Firefox 「RESTClient」 を利用します。<br>
[RESTClient](https://addons.mozilla.org/ja/firefox/addon/restclient/) を [Firefox](https://www.mozilla.org/ja/firefox/new/?utm_campaign=non-fx-button&utm_content=rta%3Ae2FkMGQ5MjVkLTg4ZjgtNDdmMS04NWVhLTg0NjM1NjllNzU2ZX0&utm_medium=referral&utm_source=addons.mozilla.org) で開き、ダウンロードしてインストールしてください。<br>

@img[span-70](template/img/environment/RestClient-add.png)
@snapend
---
@snap[north-west text-06]
### テキストエディタの準備①
@snapend

@snap[midopoint text-05]
テキストエディタは、普段ご利用のものをお使いください。<br>
この講座では [Visual Studio Code](https://code.visualstudio.com/) を利用しています。<br>

@img[span-70](template/img/environment/vscode.png)

@snapend

---
@snap[north-west text-06]
### テキストエディタの準備②アドインの追加
@snapend

@snap[midopoint text-05]
Visual Studio Code に [Elixirのアドイン](https://marketplace.visualstudio.com/items?itemName=mjmcloug.vscode-elixir) を追加します。<br>

@img[span-70](template/img/environment/vscode-elixir.png)
@snapend

---
@snap[north-west text-06]
### CUIからエディタを起動するための準備
@snapend

@snap[midopoint text-05]
Visual Studio Codeを開いた状態で<br>
Command + Shift + P で検索窓を開きます。<br>

@img[span-70](template/img/environment/vscode-adin.png)
@snapend
---
@snap[north-west text-06]
### Shell Command install
@snapend

@snap[text-05]
「Shell Command: install 'code' command in PATH」を選択します。<br>
@img[span-90](template/img/environment/vscode-shell.png)
@snapend

---
@snap[north-west text-06]
### CUI
@snapend

@snap[text-05]
CUIとは:コマンドベースの入力インターフェイス<br>
WindowsとMacでは、利用するアプリや利用するコマンドが若干異なります。<br>
＊ Windows->コマンドプロンプト<br>
＊ Mac->ターミナル<br>

@img[span-60](template/img/environment/terminal.png)
@snapend

---?color=#000000
@snap[north-west text-06 text-white]
### ターミナルの使い方
@snapend


@snap[midpoint text-06]

現在のフォルダ内にある内容の確認

@gist[terminal](Yoosuke/ef45e8a06367c20cff7b4a46714fbd12)
@[3](現在のフォルダの中を表示する（Macの場合）) 
@[5](現在のフォルダの中を表示する（Windowsの場合）) 
@[8](フォルダを作成する)
@[11](フォルダを移動する)


@snapend

---?color=#000000

@snap[north-west text-06 text-white]
### CUIからエディタを起動する方法
@snapend

@snap[midpoint]
Visual Studio Codeが起動すればOKです。<br>

@gist[zoom-10](Yoosuke/6d2cfefcc23d71cf0911074a99787e88&size=100%)
@[2]
@[5](Visual Studio Codeを立ち上げる)

@snapend

---
@snap[north-west text-06]
### Elixirのインストール
@snapend

@snap[text-05]
今回は Elixir という言語を利用しますので、お使いの環境に合わせて<br>
[インストール](https://elixir-lang.org/install.html) してください。<br>
elixirに必要なパッケージ類も一緒にインストールされます。<br>

@img[span-60](template/img/environment/elixir-hp.png)


@snapend
---
@snap[north-west text-06]
### HomeBrewのインストール for Mac
@snapend

@snap[midpint text-07]
Macの場合は [homebrew](https://brew.sh/index_ja) を使用すると便利です。　<br>
インストール方法は次で説明します。<br>

@img[span-60](template/img/environment/elixir-install-mac.png)<br>


@snapend

---?color=#000000
@snap[north-west text-06]
### Elixirのインストール for Mac
@snapend

@snap[midpoint]
homebrew からElixirをインストールします。<br>

@gist[elixir zoom-10](Yoosuke/0abcd22f59dc8cc7c0db4509aa358253)
@[1](HomebrewをUpdateする)
@[2](Elixirをインストールする)

@snapend
---
@snap[north-west text-06]
### Elixirのインストール for Windows
@snapend

@snap[midpoint text-06]
[Download the installer](https://elixir-lang.org/install.html#windows) より<br>
ダウンロードします。<br>

@img[span-90](template/img/environment/elixir-install-win.png)<br>

@snapend
---
@snap[north-west text-06]
### node.jsのインストール
@snapend

@snap[text-05]
[nodejs](https://nodejs.org/en/download/) をダウンロードします。<br>

@img[span-70](template/img/environment/nodejs.png)<br>


@snapend

---
@snap[north-west text-06]
### PostgreSQLのインストール
@snapend

@snap[text-05]
今回は、[PostgreSQL version 11.1](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads) をダウンロードします。<br>
セットアップウィザードのパスワードには *postgres* を設定します。<br>

@img[span-60](template/img/environment/postgresql.png)
@snapend
---
@snap[north-west text-06]
### Phoenixframeworkのインストール①
@snapend

@snap[text-05]
Webのフレームワークとして、[Phoenix](https://phoenixframework.org/) を利用します。<br>
インストール方法は次で説明します。<br>

@img[span-70](template/img/environment/phoenix.png)

@snapend

---?color=#000000
@snap[north-west text-06 text-white]
### Phoenix Frameworkのインストール②Phoenix v1.4のインストール
@snapend

@snap[midpoint]
CUIからコマンドを入力してインストールします。<br>
@gist[elixir midpoint zoom-16](Yoosuke/02ec19b92d74e666fd6e47e7095dfd9c)
@[1](Phoenix v1.4をインストールする)

@snapend

---?color=#000000
@snap[north-west text-06 text-white]
### Phoenix Frameworkのインストール③Phoenix プロジェクトの作成
@snapend

@snap[midpoint]

@gist[zoom-06](Yoosuke/a3b22fb6c27ef03d978d37bc80e88618)
@[1](gismapという名前でプロジェクトを作成する)
@[3](Yを入力する)
@[7](gismapのディレクトリに移動する)
@[11](DBを作成する)
@[15](サーバーを起動する)

@snapend
---
@snap[north-west text-06]
### Phoenix Frameworkのインストール④WebServerの確認
@snapend

@snap[text-05]
ブラウザで「`http://localhost:4000`」にアクセス。<br>
Phoenixで作られたデフォルトのWebページが表示される事を確認しましょう。<br>
無事に見られたら、成功です。<br>

@img[span-60](template/img/environment/localhost4000.png)

@snapend



