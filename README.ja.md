# AISストリーム API

AISデータをリアルタイムに受信し、CSV形式で出力するDeno製アプリケーションです。

## 機能

- AISデータのリアルタイム受信
- 最新の位置情報と船舶静的情報をCSV形式で出力
- サンプルデータの提供

## 必要環境

- [Deno](https://deno.land/)

## 使い方

1. [aisstream.io](https://aisstream.io/)からAPI_KEYを取得し、".env"ファイルに保存します。
2. Denoを使用してデータを受信します。
```
deno run -A receiveData.js
```
3. 最新のCSVデータファイルを生成します。
```
deno run -A make_latestPosition.js
deno run -A make_latestShipStatic.js
```
4. ブラウザでマップを表示します。
```
deno run -A https://taisukef.github.io/liveserver/liveserver.js 7777
```
[http://[::]:7777/](http://[::]:7777/)にアクセスします。

## データ・API

- AISデータはaisstream.ioのストリーミングAPIを使用しています。
- サンプルデータは"sample"ディレクトリに格納されています。

## ライセンス

MIT License