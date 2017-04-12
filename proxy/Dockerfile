# メインイメージ
FROM nginx:latest
# 製作者
MAINTAINER harurunn

# nginxのconf.defaultをリネーム
RUN mv /etc/nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf.origin
# proxy.confを/etc/nginx/conf.d/にコピー
COPY proxy.conf /etc/nginx/conf.d/
# nginxをフォアグラウンドでたちあげ、設定ファイルはnginx.confを使用する
ENTRYPOINT /usr/sbin/nginx -g 'daemon off;' -c /etc/nginx/nginx.conf
