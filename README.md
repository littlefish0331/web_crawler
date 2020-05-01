# README

這個專案要記錄我練習爬蟲的過程。  
包括

- 使用什麼語言: R, Python, bash, Go, java
- 爬取網站網址: 
- 專案名稱(repository): 連結
- 學習技能:
  - 簡單描述爬取這個網站過程學習的技巧
  - 整理該網站資料的方式
- 資料用途、爬取動機

## 目標

先設立一些小目標

- 網站數量: 5, 10, 20, 40, 60, 100
- PTT: beauty, Hate, Gossiping, Boy-Girl
- New: 蘋果, 自由, 中時, 聯合, 經濟, router, 鏡周刊
- 台灣證券交易所
- youtube 音效庫
- mask-dedicate
- blogger
- medium
- facebook

---

## 專案描述

- 專案名稱(repository): 為公司專案，無法提供。本機留有資料備份 MOD_project/lonlat/
- 使用什麼語言: R
- 爬取網站網址: [https://redtsai.blogspot.com/](https://redtsai.blogspot.com/)
- 資料用途、爬取動機: 好玩，想嘗試如何從該blog的取得資料。
- 學習技能:
  - 學習使用網址做query，在網址後面加上 "/search?max-results=30"
  - 全部為文字資料，儲存成 .txt，檔名為 blog的文章名稱
  - 建立爬取列表 [filename, url, title]，方便後續追查資料來源，已經是否有爬取過該網址。
  - 透過html去抓取網頁資訊，包括選取節點等。read_html(), html_nodes(), html_attr()
  - 將 html 的<br> ，替換成\n。xml_find_all(), xml_add_sibling(), xml_remove()
- 半角空白的 raw 為 c2 ao, 半形空白的 raw 為 20, 全形空白的 raw 為 a1 40
- unicode編碼轉換為UTF-8編碼。unicode2utf8()

