```uml
@startuml

skinparam class {
    '図の背景
    BackgroundColor Snow
    '図の枠
    BorderColor Black
    'リレーションの色
    ArrowColor Black
}

!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue

package "ECサイト" as target_system {
    /'
      マスターテーブルを M、トランザクションを T などで表記
      １文字なら "主" とか "従" まど日本語でも記載可能
     '/

    entity "ユーザーテーブル" as user <user> <<M,MASTER_MARK_COLOR>> {
        + user_number [PK]
        --
        user_id
        user_pass
        user_name
        user_address
    }
    
    entity "商品テーブル" as merchandise <merchandise> <<M,MASTER_MARK_COLOR>> {
        + genre_id [PK]
        + merchandise_id [PK]
        --
        genre_name
        merchandise_name
        int
        merchandise_detail
        sales
    }
    
    entity "履歴テーブル" as history  <history> <<T,TRANSACTION_MARK_COLOR>> {
        + history_user_number[PK]
        + history_count[PK]
        --
        # history_genre_id [FK]
        # history_merchandise_id [FK]
        history_quantity
        histoty_day
    }
    
    entity "カートテーブル" as cart <cart> <<T,TRANSACTION_MARK_COLOR>> {
        + cart_user_number[PK]
        + cart_count[PK]
        --
        # cart_genre_id [FK]
        # cart_merchandise_id [FK]
        cart_quantity
    }
    
     entity "カテゴリマスタ" as category <m_category> <<M,MASTER_MARK_COLOR>> {
        + category_id [PK]
        --
        name
        reg_date
    }
  }
  
  user       |o-ri-o{     merchandise
merchandise          ||-ri-|{     history
history    }-do-||     cart
cart          }o-le-||     category

@enduml
```
