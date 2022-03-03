RailsTemplate

## 概要
Railsアプリを作る雛形

## Docker

### イメージビルド
```shell
$ docker-compose build --no-cache
```

### 通常モード
```shell
$ app rails new . --force --no-deps --database=mysql --skip-bundle
```

### APIモード
```shell
$ app rails new . --force --no-deps --api --database=mysql --skip-bundle
```

### DBの設定

```shell
$ 
```