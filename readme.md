我想要開發一個記帳工具，記帳工具需要串接 Google 試算表

## 資料內容
### Google 試算表資料格式
Google 試算表上有兩個工作表，[記帳紀錄] 及 [欄位表]
[記帳紀錄] 工作表內容如下：
```
ID	Date	Type	Category	Amount	Description	Payment
1	2026-01-01	收入	其他雜項	55000	1 月份薪資收入	簽帳金融卡 (Debit Card / ATM 轉帳)
2	2026-01-01	支出	居家生活	12000	1 月份房租	簽帳金融卡 (Debit Card / ATM 轉帳)
3	2026-01-02	支出	餐飲食品	120	早餐店蛋餅大冰奶	現金 (Cash)
4	2026-01-02	支出	交通運輸	50	捷運通勤	電子票證 (悠遊卡, 一卡通)
5	2026-01-03	支出	休閒娛樂	330	電影票	信用卡 (Credit Card)
6	2026-01-03	支出	餐飲食品	250	晚餐拉麵	電子支付 (LINE Pay, Apple Pay, 街口支付)
7	2026-01-05	支出	居家生活	850	台電電費	信用卡 (Credit Card)
8	2026-01-06	支出	醫療保健	200	感冒診所掛號費	現金 (Cash)
9	2026-01-07	支出	購物服飾	1980	運動鞋	信用卡 (Credit Card)
```
- ID 屆時使用 timestamp 作為唯一碼
- Type 僅能輸入 收入、支出 兩個選項
- Amount 輸入數值金額
- Description 為純文字描述
- Category、Payment 則會從欄位表對應

[欄位表] 工作表內容如下：
```
Type	Category	Payment
支出	餐飲食品	現金 (Cash)
收入	交通運輸	信用卡 (Credit Card)
	居家生活	簽帳金融卡 (Debit Card / ATM 轉帳)
	休閒娛樂	電子支付 (LINE Pay, Apple Pay, 街口支付)
	學習成長	電子票證 (悠遊卡, 一卡通)
	醫療保健	
	購物服飾	
	其他雜項	
```
- 此表用於欄位選項

### 前端技術
- 請協助提供 HTML、CSS、JavaScript 的檔案，並說明放置的位置
- 我會準備 Google OAuth Client ID、試算表路徑，請提供變數讓我填寫



## 預期的結果
- 我可以登入自己的 Google 試算表
- 我可以記錄每天的帳務
- 我可以透過分類的方式，了解我的款項主要集中在哪一個項目上
- 我可以檢視每月的支出、收入表