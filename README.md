# ProtoSpace

## users テーブル
| Column             | Type   | Options     |
|--------------------|--------|-------------|
| nickname           | string | null: false |
| email              | string | null: false |
| encrypted_password | string | null: false |

## prototypes テーブル
| Column     | Type       | Options                        |
|------------|------------|--------------------------------|
| title      | string     | null: false                    |
| catch_copy | string     | null: false                    |
| concept    | text       | null: false                    |
| user_id    | references | null: false, foreign_key: true |

## comments テーブル
| Column       | Type       | Options                        |
|--------------|------------|--------------------------------|
| content      | string     | null: false                    |
| prototype_id | references | null: false, foreign_key: true |
| user_id      | references | null: false, foreign_key: true |