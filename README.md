# Tokenised Hiragana of 1714 of Japan's Municipalities' Placenames List (日本地方自治体の地名のトークン化されたリスト)  
  
Consider the town Kakuda-Shi `角田市`.  
This is written in datasets and dictionaries as `かくだし`.  
Is that broken down as `か,く,だし`, or `かく,だ,し`?  
A Japanese person will know that it is the latter intuitively.  
  
Testing NLP and AI modules, less than 40% were accurate across the 1737 entries in this list. This is because of the irregular pronunciations used for kanji when they are used in placenames. `角田市` is easy to identify; many placename kanji readings deviate significantly from common readings, to the point that manually referencing dictionaries becomes necessary.  
  
I manually tokenised these placenames as such. There is a JSON with keys, a JSON as objects, and a CSV for GUI editing. Because I've done it by hand, and because I'm not Japanese, there may be some discrepancies.  
  
# Format

```json
{
   "code": 292010,
   "name_kanji": "奈良市",
   "name_kana": "ならし",
   "name_kana_breakdown": "な,ら,し",
   "name_romaji": "Nara Shi",
   "prefecture_kanji": "奈良県",
   "prefecture_kana": "ならけん",
   "prefecture_kana_breakdown": "な,ら,けん",
   "prefecture_romaji": "Nara Ken",
   "latitude": 34.68333333,
   "longitude": 135.8
 },
 {
   "code": 292028,
   "name_kanji": "大和高田市",
   "name_kana": "やまとたかだし",
   "name_kana_breakdown": "やまと,たか,だ,し",
   "name_kana_notes": "Irregular reading: 大和 (やまと) does not decompose to two separate kanji readings",
   "name_romaji": "Yamatotakada Shi",
   "prefecture_kanji": "奈良県",
   "prefecture_kana": "ならけん",
   "prefecture_kana_breakdown": "な,ら,けん",
   "prefecture_romaji": "Nara Ken",
   "latitude": 34.5,
   "longitude": 135.7333333
 },
```

# Acknowledgements

This dataset is built upon Fabio Crisci's [open-data-jp-municipalities](https://github.com/piuccio/open-data-jp-municipalities). That list was extracted from the [Gazetteer of Japan 2007/2018](http://www.gsi.go.jp/ENGLISH/pape_e300284.html), the original 2007 Github repo of which can be found [here](https://github.com/nyampire/Gazetteer_JP_2007). Prefecture information comes from [here](http://www.soumu.go.jp/denshijiti/code.html).
