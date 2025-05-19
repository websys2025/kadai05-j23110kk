## 外部APIの呼び出しのミニレポート
### Q3-1. 郵便番号APIについて説明せよ。
* エンドポイントと機能
**エンドポイント：**`エンドポイント: https://zipcloud.ibsnet.co.jp/api/search`
**機能：**郵便番号を指定すると、**対応する住所**を取得できる。

* リクエストとレスポンスのフォーマット
**リクエスト(例)**
`GET https://zipcloud.ibsnet.co.jp/api/search?zipcode=1000001`
**レスポンス：**json(例)
`{
  "message": null,
  "results": [
    {
      "zipcode": "1000001",
      "address1": "東京都",
      "address2": "千代田区",
      "address3": "千代田",
      "kana1": "ﾄｳｷｮｳﾄ",
      "kana2": "ﾁﾖﾀﾞｸ",
      "kana3": "ﾁﾖﾀﾞ"
    }
  ],
  "status": 200
}`

### Q3-2. 各自で調査したAPIについて説明せよ。
* APIの名称と参照URL
**名称：**PokeAPI
**参照URL：**https://pokeapi.co

* エンドポイントと機能
**エンドポイント：**https://pokeapi.co/api/v2/pokemon/{id or name}/
**機能：**ポケモンの名前や図鑑番号などが取得できる。
* リクエストとレスポンスのフォーマット
**リクエスト(例)**
`GET https://pokeapi.co/api/v2/pokemon/25`

**レスポンス**
`{
  "name": "pikachu",
  "sprites": {
    "front_default": "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/25.png"
  },
  "types": [
    { "type": { "name": "electric" } }
  ]
}`

### Q3-3. 感想
* 今回の課題で苦労したこと
APIを動かすのに必要な**パラメータ**を送信するのに苦労した。
課題2でAppIDを必要とせず、無料のAPIを探すのに苦労した
* 演習を通して理解できたこと
APIを活用することで、自分でもそれっぽいアプリケーションが作れると実感できた。
* Web APIの利便性や課題など
外部の高機能なサービスを簡単に組み込めるのが非常に便利と感じた。
