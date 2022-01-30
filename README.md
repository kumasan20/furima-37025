# テーブル設計

## users テーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| nickname           | string | null: false |
| email              | string | null: false |
| encrypted_password | string | null: false |
| name               | string | null: false |
| birthday           | string | null: false |


### Association

- has_many :items
- has_many :comments

## comments テーブル

| Column | Type   | Options     |
| ------ | ------ | ----------- |
| text   | string | null: false |

### Association

- belongs_to :item
- belongs_to :user

## items テーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| product_name       | string | null: false |
| category           | string | null: false |
| price              | string | null: false |
| seller             | string | null: false |
| image              | text   | null: false |

### Association

- has_many :comments
- belongs_to :user

差分確認
