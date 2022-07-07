# 【README】

# アプリ名 ：snow-money

# アプリケーション概要： スノースポーツの支出の把握

# URL ：

# テスト用アカウント ：

# 利用方法 ：

# なぜsnow-moneyが必要か？ ：

# 要件定義 ：https://docs.google.com/spreadsheets/d/139Z2VIIpuf7Vy7dABXlDojl-17xsATGxyonjvaabClk/edit#gid=982722306

# DB設計 ：

## usersテーブル

| Column                | Type        | Options                   |
| --------------------- | ----------- | ------------------------- |
| name                  | string      | null: false , unique: true|
| email                 | string      | null: false               |
| encrypted_password    | string      | null: false               |


### Association
- has_many :trips

## tripsテーブル

| Column                  | Type        | Options                        |
| ----------------------- | ----------- | ------------------------------ |
| ski-lift                | integer     |                                |
| highspeed-rate          | integer     |                                |
| gosoline-fee            | integer     |                                |
| food-expenses           | integer     |                                |
| Miscellaneous-expenses  | integer     |                                |
| ski-resort              | string      |                                |
| uesr-id                 | references  | null: false , foreign_key: true|


### Association
- belongs_to :user
- has_one :comment

## commentsテーブル

| Column                | Type        | Options                        |
| --------------------- | ----------- | ------------------------------ |
| memo                  | text        |                                |
| trip-id               | references  | null: false , foreign_key: true|


### Association
- belongs_to :trip

# 開発環境 ：

# 工夫したポイント ：


