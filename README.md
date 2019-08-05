# README

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

## membersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|integer|null: false, foreign_key: true|

### Association
- has many : messeges
- has many : groups, through: :menbers
- has many :menbers


## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|integer|null: false, foreign_key: true|

### Association
- has many :messeages
- has many :users.through: :members
- has many :menbers


##  messagesテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|references|null: false,  foreign_key: true|
|body|text||
|image|string||


### Association
- belong_to :group
- bulomg_to :user

