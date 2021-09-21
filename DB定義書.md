## ユーザーテーブル(user)

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|ユーザー番号|user_number|int(auto_increment)|○|||
|ユーザーID|user_id|varchar(255)||○||
|ユーザーパスワード|user_pass|varchar(255)||○||
|ユーザー名|user_name|varcher(255)||○||
|ユーザー住所|user_address|varcher(255)||○||

## 商品テーブル(merchandise)

|和名|属性名(カラム名)|型|PK|NN|FK|
|---|-----|--|--|--|--|
|ジャンルID|genre_id|int|○|||
|商品ID|merchandise_id|int|○|||
|ジャンル名|genre_name|varchar(255)||○||
|商品名|merchandise_name|varcher(255)||○||
|価格|int|int||○||
|商品詳細|merchandise_detail|varcher(500)||○||
|売上|sales|int||○||
