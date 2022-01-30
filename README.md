# テーブル設計

## users テーブル

| Column             | Type   | Options                   |
| ------------------ | ------ | ------------------------- |
| nickname           | string | null: false               |
| email              | string | null: false, unique: true |
| encrypted_password | string | null: false               |
| first_name         | string | null: false               |
| last_name          | string | null: false               |
| birthday           | date   | null: false               |


### Association

- has_many :items
- has_many :comments
- has_many :purchase_managements


## comments テーブル

| Column | Type   | Options     |
| ------ | ------ | ----------- |
| text   | string | null: false |

### Association

- belongs_to :item
- belongs_to :user

## items テーブル

| Column             | Type    | Options     |
| ------------------ | ------- | ----------- |
| product_name       | string  | null: false |
| explanation        | string  | null: false |
| category_id        | integer | null: false |
| price              | integer | null: false |
| seller             | string  | null: false |
| delivery_charge    | string  | null: false |
| area               | string  | null: false |
| days               | string  | null: false |
| user_id            | string  | null: false |

### Association

- has_many :comments
- belongs_to :user

差分確認
