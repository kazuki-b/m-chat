# README

## usersテーブル

| Column          | Type    | Options     |
| --------------- | ------- | ----------- |
| nickname        | string  | null: false |
| email           | string  | null: false |
| password        | string  | null: false |
| last_name       | string  | null: false |
| first_name      | string  | null: false |
| last_name_kana  | string  | null: false |
| first_name_kana | string  | null: false |
| birthday        | date    | null: false |
| age_id          | integer | null: false |
| genre_id        | integer | null: false |

### Association
- has_many : musics
- belongs_to_active_hash : genre
- belongs_to_active_hash : age

## musicsテーブル

| Column     | Type      | Options                        |
| ---------- | --------- | ------------------------------ |
| name       | string    | null: false                    |
| artist     | string    | null: false                    |
| comment    | string    | null: false                    |
| url        | string    | null: false                    |
| image      | integer   | null: false                    |
| genre_id   | integer   | null: false                    |
| average_id | integer   | null: false                    |
| user       | reference | null: false, foreign_key: true |

### Association
- belongs_to : user
- belongs_to_active_hash : genre
- belongs_to_active_hash : average