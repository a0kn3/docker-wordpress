# wordpress


## build
```
docker-compose up -d --build
```
## M1,2 Macの場合

エラー文
```
% docker-compose up -d --build
no matching manifest for linux/arm64/v8 in the manifest list entries
```
以下を追加
```
db:
    platform: linux/x86_64    //追加
    container_name: test-db
    image: mysql:5.7
```

## URL
立ち上げ後、少し待ってからアクセス  
```
http://localhost:8000
```

## 参考
[docker hub](https://hub.docker.com/_/wordpress/tags?page=1&name=php8.1)  
[バージョン管理](https://webgaku.net/jp/wordpress/requirements/)  
[コンテナエラー確認](https://ysko909.github.io/posts/docker-container-gets-into-restarting-loop/)  
[DBエラー](https://qiita.com/kazumawada/items/dec8cf5b96dbaf4992f0)  
[docker-compose.ymlでwordpress](https://www.distant-view.co.jp/column/6623/)  




