# traffic-accident-converter
- 本プログラムは、警察庁が公開している、[交通事故統計情報のオープンデータ（2019年、2020年、2021年）の本票](https://www.npa.go.jp/publications/statistics/koutsuu/opendata/index_opendata.html)を[コード表](https://www.npa.go.jp/publications/statistics/koutsuu/opendata/index_opendata.html)を元に読みやすいデータに変換するプログラムになります。
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
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/honhyo_2019-2021.csv`

#### 出力結果
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/honhyo_2019-2021_to-degree.csv`

### csvfile-convert.py
- 十進法度単位に変換した本票CSVファイル（2019～2021年）をコード表を元に読みやすいデータに変換するプログラムになります。

#### 使用データ
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/honhyo_2019-2021_to-degree.csv`
- コード表`https://github.com/shi-works/traffic-accident-converter/tree/main/code`

#### 出力結果
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/honhyo_2019-2021_convert_v2.csv`

### 使用データ及び出力結果のライセンスについて
本データセットは[CC-BY-4.0]で提供されます。使用の際には本レポジトリへのリンクを提示してください。

また、本データセットは交通事故統計情報のオープンデータ（2019年、2020年、2021年）の本票を加工して作成したものです。本データセットの使用・加工にあたっては、[警察庁Webサイトの利用規約](https://www.npa.go.jp/rules/index.html)を確認し、権利者の権利を侵害しないように留意してください。
