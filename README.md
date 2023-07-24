# List Detailing 1714 of Japan's Municipalities' Placenames with Tokenised Hiragana (日本地方自治体の地名のトークン化された平仮名からなるデータセット)  
  
Consider the town Kakuda-Shi `角田市`.  
This is written in datasets and dictionaries as `かくだし`.  
Is that broken down as `か,く,だし`, or `かく,だ,し`?  
A Japanese person will know that it is the latter intuitively.  
  
NLP and AI parsers were highly innaccurate identifying the context-specific reading of a given placename-nested kanji across the 1737 entries in this list (1714 municipalities + 23 regional subdivision 'wards' of Tokyo). This is because many placename kanji readings deviate significantly from common readings. 
  
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

