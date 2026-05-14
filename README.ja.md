# AIS Stream API

AIS Stream APIは、リアルタイムのAISデータを受信・処理し、最新の位置情報と船舶静的情報をCSV形式で提供するDenoベースのアプリケーションです。

## 使い方

1. [aisstream.io](https://aisstream.io/) からAPI_KEYを取得し、".env"ファイルに記述します。
```
AISSTREAM_API_KEY=xxxxxxxxx
```

2. [Deno](https://deno.land/) を使用してaisstreamからデータを受信します。
```
deno run -A receiveData.js
```

3. 最新のCSVデータファイルを生成します。

```
deno run -A make_latestPosition.js
deno run -A make_latestShipStatic.js
```

4. ブラウザでマップを確認します。
```
deno run -A https://taisukef.github.io/liveserver/liveserver.js 7777
```
[http://[::]:7777/](http://[::]:7777/) を開きます。

## データ / API

- AISデータは、aisstream.ioのストリーミングAPIから取得しています。
- サンプルデータは "sample" ディレクトリに保存されています。

## ライセンス

MIT License — 詳細は [LICENSE](LICENSE) を参照してください。
