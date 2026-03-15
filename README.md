# AIS Stream API

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

The AIS Stream API is a Deno-based application that receives and processes real-time AIS data, providing the latest position and ship static information in CSV format.

## Demo

- [https://code4fukui.github.io/aisstream/](https://code4fukui.github.io/aisstream/) at 2023-10-23

## Sample JSON Data

- [sample](sample)

## Usage

1. Get your API_KEY from [aisstream.io](https://aisstream.io/) and write it to the ".env" file.
```
AISSTREAM_API_KEY=xxxxxxxxx
```

2. Receive data from the aisstream via [Deno](https://deno.land/).
```
deno run -A receiveData.js
```

3. Generate the latest CSV data files.

```
deno run -A make_latestPosition.js
deno run -A make_latestShipStatic.js
```

4. Check the map on your browser.
```
deno run -A https://taisukef.github.io/liveserver/liveserver.js 7777
```
open [http://[::]:7777/](http://[::]:7777/)

## Data / API

- The AIS data is obtained from the aisstream.io streaming API.
- Sample data is stored in the "sample" directory.

## License

MIT License