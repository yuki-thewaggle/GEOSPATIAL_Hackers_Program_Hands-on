### APIServerの構築

gismapというプロジェクト名でフェニックスのプロジェクトを作る

```
mix phx.new gismap
Fetch and install dependencies? [Yn] （←y、Enterを入力）
```

---

```cd gismap```
で、プロジェクトに移動

次にDBを作ります。
```
mix ecto.create
```
---

### サーバーを立ち上げる
サーバーが起動するか確認のため下記コマンドで立ち上げる
```
iex -S mix phx.server
```
立ち上がっているか
localhost:4000
をブラウザで開いて確認します。

---

![ブラウザの様子](template/Building-APIServer/1-terminal.png)

サーバーを終了するには
Ctrl+C を2回打つ

---
### 緯度と経度と名称を入れるためのJSONを作る
下記のコマンドを入力
```
mix phx.gen.json Api Location locations lat:float lng:float pointname:string
```
---

次に表示された通りにファイルを開きます

```
Add the resource to your :api scope in lib/gismap_web/router.ex:

    resources "/locations", LocationController, except: [:new, :edit]


Remember to update your repository by running migrations:

    $ mix ecto.migrate
```

@[3](ファイルに追加するのでコピーしておきます。)
---
### VSCODEでファイルを開く

```
code .
```
コマンドを入力し、VSCODEを立ち上げ

```
lib/gismap_web/router.ex
```

のファイルを開きます

---?color=#1E1F21
@code[elixir zoom-4](template/src/elixir/router.ex)

@[8](コメントアウトする)
@[20](ここに先ほどコピーした内容をペーストします)

---
### マイグレーションする

```
mix ecto.migrate
```

テーブルが作成されます

```
[info] == Running 20190110032559 Gismap.Repo.Migrations.CreateLocations.change/0 forward
[info] create table locations
[info] == Migrated 20190110032559 in 0.0s
```

---
### サーバー立ち上げる

Phoenixを起動します

```
iex -S mix phx.server
```

---
### FirefoxのRESTClientを使ってgetのリクエストを投げる

REST APIクライアントを利用して、APIサーバーにデータを入れます。
Firefoxを立ち上げ、RESTClientを起動します。

---?color=#333333

RESTClientの「Headers」メニューで、「Custom Header」を選択

Nameに　``` Content-Type ```

Attribute Valueには　``` application/json ```

を入力します。

---
### 帰ってきたデータ形式を確認

まだ、データは何も入っていないので、次のような状態になります。

```

{"data":[]}

```

![画面キャプチャ]()

---
### RESTClientを使ってデータをPOSTする

Methodの所を「POST」に変更します。



---
緯度と経度と名称を入れるためのJSONを作る
 マイグレーションする
 サーバー立ち上げる
Firefoxのゲストクライアントを使ってgetのリクエストを投げる
帰ってきたデータ形式を確認
lestレストクライアントを使って緯度と経度と名前のデータをpostする
local　host に対してgetリクエストする
postしたデータがgetできるか確認


