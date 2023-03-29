# traffic-accident-converter
- 本プログラムは、警察庁が公開している、[交通事故統計情報のオープンデータ（2019年、2020年、2021年）の本票](https://www.npa.go.jp/publications/statistics/koutsuu/opendata/index_opendata.html)をコード表を元に読みやすいデータに変換するプログラムになります。
- Pythonで構築

## プログラムについて

### csvfile-merge.py
- 本票CSVファイル（2019年、2020年、2021年）をマージするプログラムになります。

#### 使用データ
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/data/honhyo_2019.csv`
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/data/honhyo_2020.csv`
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/data/honhyo_2021.csv`

#### 出力結果
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/honhyo_2019-2021.csv`

### csvfile-to-degree.py
- マージした本票CSVファイル（2019～2021年）の「地点　緯度（北緯）」と「地点　経度（東経）」を十進法度単位に変換するプログラムになります。

#### 使用データ
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/data/honhyo_2019.csv`
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/data/honhyo_2020.csv`
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/data/honhyo_2021.csv`

#### 出力結果
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/honhyo_2019-2021.csv`
