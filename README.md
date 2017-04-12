# Nginx+リバースプロキシサンプル

## 構成
- docker
  - proxy
    - docker-compose.yml
    - Dockerfile
    - proxy.conf
  - webapp
    - web
    - docker-compose.yml
  - webapp2
    - web
    - docker-compose.yml  

#### ディレクトリ内訳
##### proxy：  
Nginxを用いたリバースプロキシサーバです。  
ホストのポート80番へのアクセスは全てここに流れます。

##### webapp：  
リバースプロキシから振り分ける先のサーバです。  
今回はwebアプリケーションを想定していてwebapp/webがnginxの公開ディレクトリとシンボリックリンクみたいな感じになっているのでそこにindex.htmlなどを配置します。

##### webapp2：
webappと同じです。  
こちらでは違うwebサービスを立ち上げていると想定しています。

## 使い方
時間ができたらまたコミットします
