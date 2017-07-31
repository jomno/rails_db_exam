Rails db (디버깅을 편하게) 
==
'rails db'는 개발 단계에서 유용하게 사용할 수 있는 데이터베이스 디버깅 gem입니다.<br>
상세 설명은 [rails db](https://github.com/igorkasyanchuk/rails_db) 여기를 참고하세요
## 1. 더미 데이터(실제 사용 시 적용 X)
* bash - model 만들기
```bash
rails g model user name age:integer
rails g model post title content:text user:references
rails g model comment body post:references user:references
rake db:migrate
```
가상의 user, post, comment 모델 생성
## 2. rails db 적용
* Gemfile
```ruby
gem 'rails_db'
```
* bash 
```bash
bundle install
rails s
```
이후 [주소/rails/db](주소/rails/db) 접속하면 rails db 페이지 접속
<img src="https://raw.githubusercontent.com/igorkasyanchuk/rails_db/master/docs/main_view.png?token=AAArXeu9-vtuW8nIvc9RE0nOIhGbwxkbks5WKlTLwA%3D%3D"
/>
## Reference post
[rails db](https://github.com/igorkasyanchuk/rails_db)