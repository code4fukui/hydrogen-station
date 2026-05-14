# hydrogen-station

日本の水素ステーションに関するオープンデータとサンプル地図を提供するプロジェクトです。データは毎日自動更新されます。

## ライブデモ

- [水素ステーション地図](https://code4fukui.github.io/hydrogen-station/sample/)

このインタラクティブな地図は、データセットに含まれるすべての水素ステーションの位置を表示します。

## オープンデータ

水素ステーションのデータは以下の形式で提供されています：

- **[JSON](https://code4fukui.github.io/hydrogen-station/data/hydrogen-station-info.json)**
- **[CSV](https://code4fukui.github.io/hydrogen-station/data/hydrogen-station-info.csv)**

## 特徴

- **毎日更新**: データは毎日18:15（JST）に、[定期実行されるGitHub Action](.github/workflows/scheduled-fetch.yml)を通じて自動的に取得および更新されます。
- **複数のデータ形式**: 幅広い互換性を確保するため、データはJSONおよびCSVの両形式で提供されます。
- **インタラクティブな地図**: [csv-map](https://github.com/code4fukui/csv-map)ウェブコンポーネントを使用したサンプル実装により、ステーションデータを可視化しています。
- **豊富な情報**: 住所、営業時間、連絡先、稼働状況などの詳細情報が含まれています。

## ローカル開発

ローカルでデータ取得スクリプトを実行する手順は以下の通りです：

1.  **前提条件**: [Deno](https://deno.land/)ランタイム（v1.x）をインストールします。
2.  **リポジトリのクローン**:
    ```bash
    git clone https://github.com/code4fukui/hydrogen-station.git
    cd hydrogen-station
    ```
3.  **データの取得**:
    ```bash
    deno run -A deno/download.js
    ```
    これにより `/data` ディレクトリ内のファイルが更新されます。
4.  **地図の表示**: ウェブブラウザで `sample/index.html` を開きます。

## データソース

- [トヨタ MIRAI | 水素ステーション | トヨタ自動車WEBサイト](https://toyota.jp/mirai/station/)

## ライセンス

このプロジェクトは[MIT License](LICENSE)の下で公開されています。
