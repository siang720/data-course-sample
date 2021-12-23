# Data course S2A2 - Rule based project
###### tags: `alphacamp data course`

### 專案目的
建立一個推薦系統，推薦商品給曾經在Mimi Beauty網站上購買過美妝商品的客戶。

### 執行方式
透過分析美妝產品資料(product data)、用戶評分資料(review data)，設計推薦邏輯，推薦商品給客戶。

### 資料切割方式
* Training data：日期在2018-09-01之前的用戶評分資料。
* Testing data：日期介於2018-09-01及2018-09-30的用戶評分資料。

### 推薦邏輯
本次專案共設計三個不同的推薦邏輯，說明如下列：
#### 1. Recommend Top 10 review number
邏輯：根據Training data，找出前10個評分數量最多的商品，將這10個商品推薦給每位目標用戶。
#### 2. Recommend Top 10 review number in past 180 days
邏輯：根據Training data，找出過去180天內，前10個評分數量最多的商品，將這10個商品推薦給每位目標用戶。
#### 3. Recommend Also buy or view product
邏輯：根據美妝產品資料歸納出每個產品(目標產品)對應的曾經購買或曾經瀏覽的產品列表。針對Traing data中曾經購買目標產品的客戶，推薦目標產品對應的產品列表給他。

### 使用工具及平台
Python, Colab

### 推薦結果
三個推薦邏輯之中，第2個邏輯分數最高，推測第2個比第1個邏輯分數高的原因，可能是美妝產品客戶有跟隨潮流購買商品的現象。
|   推薦邏輯 |      推薦分數 |
|--------------:|-----------:|
|             1 | 0.0830508  |
|             2 | 0.0966102  |
|             3 | 0.00169492 |
