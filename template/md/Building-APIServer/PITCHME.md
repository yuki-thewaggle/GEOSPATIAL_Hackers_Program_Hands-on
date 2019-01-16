---?color=#EFBB24
# @css[headline](APIサーバの構築)


---?gist=Yoosuke/a3b22fb6c27ef03d978d37bc80e88618&color=#000000
@[1](gismapという名前でプロジェクトを作成する)
@[3](Yを入力する)
@[7](gismapのディレクトリに移動する)
@[11](DBを作成する)
@[15](サーバーを起動する)

@snap[midopoint north-west text-06]
### プロジェクトファイルの生成
@snapend

---
@snap[north-west text-06]
### Webサーバの確認
@snapend

@snap[text-05]
ブラウザで「`http://localhost:4000`」にアクセス。<br>
Phoenixで作られたデフォルトのWebページが表示される事を確認しましょう。<br>
無事に見られたら、成功です。<br>

@img[span-60](template/img/environment/localhost4000.png)

@snapend

---
@snap[north-west text-06]
### サーバーの終了方法
Ctrl+C を2回打ちます。
@snapend

@img[span-60](template/img/Building-APIServer/1-ctr-c.png)

---

@snap[north-west text-06]
### JSONデータを作る
@snapend

@snap[text-05]
ターミナルで以下を打つ<br>
緯度と経度と名称を入れるためのJSONを作る<br><br>

  @color[#6F3381](mix phx.gen.json コンテキスト名 スキーマ名 スキーマ名の複数形　データ名：データ型)<br><br>

@gist[elixir midpoint zoom-15](Yoosuke/e18deaff49fd420a220bb338602160fc)

<br><br>このコマンドは、JSONリソースのcontroller, views, contextを生成します。<br><br>

詳しくは、[こちら](https://hexdocs.pm/phoenix/Mix.Tasks.Phx.Gen.Json.html)のライブラリに記載されています。
@snapend

---

@snap[north-west text-06]
### JSONデータの作成
緯度と経度と名称を入れるためのJSONデータを作ります。<br>
CUIで以下のコマンドを打ちます。
@snapend

@snap[midpoint text-07]
@gist[elixir west zoom-10](Yoosuke/e18deaff49fd420a220bb338602160fc)
@snapend


@snap[west text-06]
<br><br><br>
@color[#6F3381](mix phx.gen.json コンテキスト名 スキーマ名 スキーマ名の複数形　データ名：データ型)

<br>このコマンドは、JSONリソースのcontroller, views, contextを生成します。<br>
詳しくは、[こちら](https://hexdocs.pm/phoenix/Mix.Tasks.Phx.Gen.Json.html)のライブラリに記載されています。
@snapend

---?gist=Yoosuke/426e9d127ab84f72e0493874b7ddac77&color=#000000
@[3](ファイルに追加するのでコピーしておく)

@snap[north-west text-06　text-white]
### Router.exの設定
このコマンドは、エディタでファイルを開いて追記します。<br>
CUIでは打ちません。<br>
このコマンドをコピーしておきます。
@snapend

---?terminal=template/sessions/start-up-code.json&color=#7FDBFF&font=small&title=Visual Studio Codeでファイルを開く
@snap[north-west text-06]
### Visual Studio Codeでファイルを開く
@snapend

---
@snap[north-west text-06]
### Router.exを編集する
@snapend

![Video](https://player.vimeo.com/video/311145345)

---?color=#333333
@snap[north-west text-06]
### Router.exの編集方法
@snapend

@snap[midpoint text-05]

1. lib > gismap_web > router.ex をクリック
1. 19行目と20行目の間に改行を入れる
1. `resources "/locations", LocationController, except: [:new, :edit]` と記入
1. 8行目「plug :protect_from_forgery」の先頭に `#` を記入
1. Control + S を打ってファイルを保存

@snapend

---?color=#1E1F21
@code[elixir zoom-4](template/src/elixir/router.ex)
@[8](コメントアウト（コメント化してプログラム処理させないように）する)
@[20](ここに先ほどコピーした内容をペーストする)

@snap[north-west text-06]
### Router.exの編集方法
@snapend

---?color=#000000
@snap[north-west text-06]
### マイグレーション（データを移行）を実行
@snapend

@code[elixir midpoint zoom-10](template/src/elixir/migrate.ex)

---?color=#000000
@snap[north-west text-06]
### サーバの立ち上げ
@snapend

@code[elixir zoom-4 midpoint](template/src/elixir/start.ex)

@snap[south text-06]
Phoenixを起動
@snapend

---?terminal=template/sessions/start-server.json

---
@snap[north-west text-06]
### ブラウザで確認
localhost:4000で表示されていれば成功
@snapend

@img[span-60](template/img/Building-APIServer/5-localhost.png)

---
@snap[north-west text-06]
### RESTClientでGET、POSTの動作確認
@snapend

![Video](https://player.vimeo.com/video/311154615)

---?color=#333333
@snap[north-west text-06]
### RESTClientの設定
@snapend

@snap[midpoint text-05]

RESTClientの「Headers」メニューで、<br>
「Custom Header」を選択<br>

Nameに　``` Content-Type ```<br><br>

Attribute Valueには　``` application/json ```<br><br>

を入力します。

@snapend

---
@snap[north-west text-06]
### データの確認
@snapend

@snap[midpoint text-05]
まだ、データは何も入っていないので、次のような状態になります。

```

{"data":[]}

```
@snapend

---
@snap[north-west text-06]
### RESTClientを使ってデータをPOSTする
@snapend

@snap[text-05]
Methodの所を「POST」に変更します。
Bodyに<br>
@color[#6F3381]({ "location": { "lat": 35.70822, "lng": 131.463398, "pointname": "test" } })<br>
を入力してSENDします。<br>

@img[span-50](template/img/Building-APIServer/2-rest-post.png)

@snapend


