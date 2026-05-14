# hydrogen-station

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A project providing open data and a sample map for hydrogen stations in Japan. The data is automatically updated daily.

## Live Demo

- [Hydrogen Station Map](https://code4fukui.github.io/hydrogen-station/sample/)

This interactive map displays the location of all hydrogen stations from the dataset.

## Open Data

The hydrogen station data is available in the following formats:

- **[JSON](https://code4fukui.github.io/hydrogen-station/data/hydrogen-station-info.json)**
- **[CSV](https://code4fukui.github.io/hydrogen-station/data/hydrogen-station-info.csv)**

## Features

- **Daily Updates**: The data is automatically fetched and updated every day at 18:15 JST via a [scheduled GitHub Action](.github/workflows/scheduled-fetch.yml).
- **Multiple Formats**: Data is provided in both JSON and CSV for broad compatibility.
- **Interactive Map**: A sample implementation using the [csv-map](https://github.com/code4fukui/csv-map) web component to visualize the station data.
- **Rich Information**: Includes details such as address, operating hours, contact information, and operational status.

## Local Development

To run the data fetching script locally:

1.  **Prerequisites**: Install the [Deno](https://deno.land/) runtime (v1.x).
2.  **Clone the repository**:
    ```bash
    git clone https://github.com/code4fukui/hydrogen-station.git
    cd hydrogen-station
    ```
3.  **Fetch the data**:
    ```bash
    deno run -A deno/download.js
    ```
    This will update the files in the `/data` directory.
4.  **View the map**: Open `sample/index.html` in your web browser.

## Data Source

- [Toyota MIRAI | Hydrogen Stations | Toyota Motor Corporation Website](https://toyota.jp/mirai/station/)

## License

This project is available under the [MIT License](LICENSE).