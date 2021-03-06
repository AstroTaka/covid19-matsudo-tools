# covid19-matsudo-tools

松戸市版のツール

## 使い方

```bash
git clone https://github.com/civictechzenchiba/covid19-chiba-tools.git
cd covid19-chiba-tools
python3 -m venv venv
source venv/bin/activate
pip install -U pip
pip install -r requirements.txt
python download.py
python convert.py | jq . > data.json
```
dockerを使う場合

```bash
git clone https://github.com/civictechzenchiba/covid19-chiba-tools.git
cd covid19-chiba-tools
docker build -t chiba-covid19-tools .
docker run --rm -it chiba-covid19-tools > data.json
```
## ファイル

download.pyはdataディレクトリに[Google Drive](https://drive.google.com/drive/folders/1SxZqdYCx5vN2JUPycePzfbnW7L7VTiiS)から以下のxlsxファイルをダウンロードします。

- 検査実施サマリ.xlsx
- 検査実績（データセット）千葉県衛生研究所2019-nCoVラインリスト<日付>.xlsx
- 検査実施日別状況.xlsx
- 【<日付>】千葉県_感染者発生状況.xlsx
- 帰国者接触者センター相談件数-RAW.xlsx
- コールセンター相談件数-RAW.xlsx
