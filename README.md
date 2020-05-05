# README

這個專案要記錄我練習爬蟲的過程，包括  

- 專案名稱(repository): 連結
- 使用什麼語言: R, Python, bash, Go, java
- 爬取網站網址:
- 資料用途、爬取動機
- 爬蟲技能:
  - 簡單描述爬取這個網站過程學習的技巧
  - 整理該網站資料的方式
- 資料處理

## 目標

先設立一些小目標，目前: **3.5**

- 網站數量: 5, 10, 20, 40, 60, 100
- PTT: beauty, Hate, Gossiping, Boy-Girl
- New: 蘋果, 自由, 中時, 聯合, 經濟, router, 鏡周刊, 風傳媒, 公視, 軍聞社, 中央社
- 台灣證券交易所: [https://bsr.twse.com.tw/bshtm/](https://bsr.twse.com.tw/bshtm/)
- ~~youtube 音效庫~~
- ~~mask-dedicate~~
- 撩妹語錄: 渣男API
- blogger
- medium
- facebook
- instagram
- [雙語詞彙 - 下載專區](http://terms.naer.edu.tw/downloadlist/)

---

## 專案描述

### 專案01 - blogspot.com

- 專案名稱(repository): 為公司專案，無法提供。本機留有資料備份 MOD_project/lonlat/
- 使用什麼語言: R
- 爬取網站網址: [https://redtsai.blogspot.com/](https://redtsai.blogspot.com/)
- 資料用途、爬取動機: 好玩，想嘗試如何從該blog的取得資料。
- 爬蟲技能:
  - 學習使用網址做query，在網址後面加上 "/search?max-results=30"
  - 全部為文字資料，儲存成 .txt，檔名為 blog的文章名稱
  - 建立爬取列表 [filename, url, title]，方便後續追查資料來源，已經是否有爬取過該網址。
  - 透過html去抓取網頁資訊，包括選取節點等。read_html(), html_nodes(), html_attr()
  - 將 html 的</br>，替換成\n。xml_find_all(), xml_add_sibling(), xml_remove()
- 資料處理
  - 半角空白的 raw 為 c2 ao, 半形空白的 raw 為 20, 全形空白的 raw 為 a1 40
  - unicode編碼轉換為UTF-8編碼。unicode2utf8()
  - 地址轉經緯度: google api, google sheet(每天約一千筆限制)。

### 專案02 - 撩妹語錄收集

這可能算是一個比較大的專案，因為自己過去就有在收集這種語錄XDD  
所以趁這次用這個機會把東西整理一下

- 專案名稱(repository): 連結
- 使用什麼語言: R, Python, bash, Go, java
- 爬取網站網址:
- 資料用途、爬取動機
- 爬蟲技能:
  - 簡單描述爬取這個網站過程學習的技巧
  - 整理該網站資料的方式
- 資料處理

### 專案03 - mask dedicate

- 專案名稱(repository): [littlefish0331/mask_dedicate: web crawler mask dedicate list](https://github.com/littlefish0331/mask_dedicate)
- 使用什麼語言: R
- 爬取網站網址: [https://taiwancanhelp.com.tw/mask-dedicate](https://taiwancanhelp.com.tw/mask-dedicate)
- 資料用途、爬取動機: 想統計看看不同名字捐口罩的數量，以及捐贈趨勢變化。詳見 README.md
- 爬蟲技能:
  - query show 的筆數可以自動調整，但基本上不會抓太大。先設定每次1000筆。
  - 學習接續使用 &next 的參數，直到爬取結束。
  - 紀錄有哪些天的資料已經爬過了，以方便後續爬取的篩選。
- 資料處理

### 專案04 - youtube 音效庫

- 專案名稱(repository): [littlefish0331/YT_audiolibrary: web crawl YT audiolibrary](https://github.com/littlefish0331/YT_audiolibrary)
- 使用什麼語言: R
- 爬取網站網址: [音效庫 - YouTube](https://www.youtube.com/audiolibrary/music?nv=1)
- 資料用途、爬取動機: 想嘗試爬看看 + 想知道YT音效庫的內容，之後還可以做一個更好的介面，紀錄創作者自己的tags。詳見 README.md
- 爬蟲技能:
  - 認識動態加載網頁，以及查詢資料路徑
    - 如何取得想要的 query 網址: F12(開發人員選項) + Network + XHR + Headers和Preview
  - R 操作 cmd
  - cmd 呼叫 chrome 進行操作
    - 輸入 url，等待query後，下載完成
- 資料處理
  - R 移動檔案以及刪除
  - 解析 json 檔案
  - 特殊文字(例如法國 latin 編碼)轉換

### 專案05 - CDC 新聞
