# アプリケーション名

## taberaku

# アプリケーション概要


# テーブル設計

## menus テーブル

| Column | Type   | Options     |
| ------ | ------ | ----------- |
| name   | string | null: false |

### Association

- has_many :foodstuffs
- has_many :procedures

## foodstuffs テーブル

| Column   | Type    | Options           |
| -------- | ------- | ----------------- |
| name     | string  | null: false       |
| quantity | string  |                   |
| menu_id  | integer | foreign_key: true |

### Association

- belongs_to :menu

## procedures テーブル

| Column  | Type    | Option            |
| ------- | ------- | ----------------- |
| text    | text    | null: false       |
| menu_id | integer | foreign_key: true |

### Association

- belongs_to :menu

## refrigerate テーブル

| Column        | Type   | Option      |
| ------------- | ------ | ----------- |
| name          | string | null: false |
| quantity      | string |             |
| purchase_date | date   |             |
| best_before   | date   |             |

## frozen テーブル

| Column        | Type   | Option      |
| ------------- | ------ | ----------- |
| name          | string | null: false |
| quantity      | string |             |
| purchase_date | date   |             |
| best_before   | date   |             |

## normal テーブル

| Column        | Type   | Option      |
| ------------- | ------ | ----------- |
| name          | string | null: false |
| quantity      | string |             |
| purchase_date | date   |             |
| best_before   | date   |             |


This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
