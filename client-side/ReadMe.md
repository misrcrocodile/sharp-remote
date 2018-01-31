# TV remote Client using websocket
このウェブはシャープTVをコントロールできるように、IoTデバイスを接続して、指示を出す。今回はWebsocketを使います。

WebSocket接続を開くには、単に WebSocket コンストラクタを呼び出します。
```javascript
var connection = new WebSocket('ws://192.168.2.104:8011/', ['webClient']);

```
ws: に注目してください。これは WebSocket 接続用の新しい URL スキーマです。セキュリティで保護された WebSocket 接続用の wss: もあります。これは、https: がセキュリティで保護された HTTP 接続に使用されるのと同じです。
webClient: Websocketのプロトコールです。

今回の設定は1番めの引数を変えます。NodejsサーバーのIP Addressやポートを記入して、接続できます。

注意：ポートは８０だったら、書かなくてもいいです。
例えば、今回Herokuでサーバを立ち上げました。
```javascript
var connection = new WebSocket('wss://shrouded-peak-81739.herokuapp.com/', ['webClient']);

```