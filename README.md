RailsTemplate

## 概要
Railsアプリを作る雛形

## Docker

### 雛形作成

#### 通常モード
```shell
$ docker-compose run app rails new . --force --no-deps --database=mysql --skip-bundle
```

#### APIモード
```shell
$ docker-compose run app rails new . --force --no-deps --api --database=mysql --skip-bundle
```

### イメージビルド
```shell
$ docker-compose build --no-cache
```

## DBの作成

```shell
$ rake db:create
```