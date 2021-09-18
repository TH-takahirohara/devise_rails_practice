# README
- devise gemの実験用リポジトリ

* Version
ruby 2.5.1
rails 5.2.6
devise 4.8.0

## 参考サイト
- https://qiita.com/Hal_mai/items/350c400e8763ce0487a3
- https://qiita.com/cigalecigales/items/f4274088f20832252374

## 注意点
- redis-server起動時に、下記の指定をしないと、dump.rdbがredis-serverを起動したディレクトリに生成されてしまうので注意。（[参考](https://blog.kotamiyake.me/tech/output-dump-rdb-to-current-directory/)）
```
$ redis-server /usr/local/etc/redis.conf
```
- session storeの設定を[Githubに記載](https://github.com/redis-store/redis-rails#session-storage)の通りにすると、ActionController::InvalidAuthenticityTokenエラーが出る。secureパラメータを外すとエラーは消えた。ローカルでhttpでのみアクセスを試していたので、不要だったと思われる。
