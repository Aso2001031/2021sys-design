# DB定義書
## ER図
[ER図はこちら](https://github.com/Aso2001031/2021sys-design/blob/main/src/md/E-R図/オリジナルサイト.md "ER図はこちら")

# DBテーブルカラム詳細一覧

### 購入テーブル(o_purchase)
| 属性名 |     型    | PK | NN | FK |
|--------|-----------|----|----|----|
|オーダーID|order_id|bigint(20)|〇|〇||
|顧客コード|customer_id|int(50)||〇||
|購入日|purdhase_date|date||〇||
|総額|total_price|int(11)||〇||

### 購入詳細テーブル(o_purchase_detail)
|和名|属性名 (カラム名)|型| PK | NN | FK |
|---|-----|-----------|----|----|----|
|オーダー詳細ID|detail_id|bigint(20)|〇|〇||
|オーダーID|order_id|bigint(20)|〇|〇|〇|
|商品コード|item_id|int(50)||〇|〇|
|価格|price|int(11)||〇||
|数量|num|int(11)||〇||

### 顧客マスタ(o_customers)
|和名|属性名 (カラム名)|型| PK | NN | FK |
|---|-----|-----------|----|----|----|
|顧客コード|customer_id|int(100)|〇|〇||
|氏名|name|varchar(50)||〇||
|パスワード|pass|varchar(20)|〇|〇|〇|
|メールアドレス|mail|varchar(100)||〇||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||〇||
|ハラル認証|halal|int(11)|||

### アレルギマスタ(o_allergy)
|和名|属性名 (カラム名)|型| PK | NN | FK |
|---|-----|-----------|----|----|----|
|アレルギーID|al_id|int(100)|〇|〇||
|名前|name|varcher(50)||〇||
|登録日|reg_date|date||〇||

### 顧客アレルギマスタ(o_customers_allergy)
|和名|属性名 (カラム名)|型| PK | NN | FK |
|---|-----|-----------|----|----|----|
|顧客コード|customer_id|int(100)|〇|〇|〇|
|アレルギーID|al_id|int(100)||〇|〇|

### 商品マスタ(o_items)
|和名|属性名 (カラム名)|型| PK | NN | FK |
|---|-----|-----------|----|----|----|
|商品コード|item_id|int(100)|〇|〇||
|商品名|item_name|varchar(50)||〇||
|価格|price|int(11)||〇||
|画像ファイル名|image|varchar(200)||〇||
|商品詳細|detail|varchar(200)||||
|削除フラグ|del_flag|int(11)||||
|登録日|reg_date|date||〇||
|ハラル認証|halal|int(11)||||
