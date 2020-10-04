# freeze(仮)
食べ物の賞味期限、消費期限の管理が簡単にできるようになる。
To doリストのように簡単に使えて、
非常に便利なアプリケーション

## demo

## vs.
-Pantry Photo
https://apps.apple.com/jp/app/pantry-photo/id1210278614?mt=8

-freezeとの違い
1.freezeはトップページでアイテム削除を行うことができる

## Usage

## Install

## DB

### items
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|image|text|null: false|
|category|integer|null: false|
|user_id|integer|null: false,foreign_key: true|
#### Association
- belongs_to :user

### users
|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|email|string|null: false|
|password|string|null: false|
|password_confirmation|string|null: false|
#### Association
- has_many :items
