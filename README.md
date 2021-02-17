# テーブル設計

## users テーブル

| Colum      | Type       | Options     |
| ---------- | ---------- | ----------- |
| name       | string     | null: false |
| email      | string     | null: false |
| password   | string     | null: false |
| profile    | text       | null: false |
| occupation | text       | null: false |
| position   | text       | null: false |

### association

- has_many :prototypes
- has_many :comments

## comments テーブル

| Column     | Type       | Options     |
| ---------- | ---------- | ----------- |
| text       | text       | null: false |
| user       | references | null: false |
| prototype  | references |             |

- belongs_to :user
- belongs_to :prototype

## prototypes テーブル

| Column     | Type       | Options     |
| ---------- | ---------- | ----------- |
| title      | string     | null: false |
| catch_copy | text       | null: false |
| concept    | text       | null: false |
| user       | references |             |

- belongs_to :user
- has_many :comment



