# docker-share
## 概要
dockerのpython(django)およびPostgreSQL

### バージョン情報
python 3.10.8

PostgreSQL 14.5

## フォルダ構成
```
.
├── docker-compose.yml
├── django
    ├── Dockerfile
    └── opt
        └── test.py
└── postgresql
    ├── Dockerfile
    ├── init
        └── init.sql　#初期化用ファイル
    └── data
        └── #sql永続データ保存先(git管理対象外)
    
```


## 使い方

### docker起動コマンド
```
docker-compose up -d
```

### docker起動コマンド(dockerfile編集後)
```
docker-compose up -d --build
```

### docker停止コマンド
```
docker-compose down
```

### 起動コンテナ確認
```
docker ps
```
### コンテナログの確認
```
docker logs -f コンテナ名  
```

### コンテナ内に入る
```
docker-compose exec コンテナ名 bash  
```

### なぜかうまくいかない時
```
docker system prune
```