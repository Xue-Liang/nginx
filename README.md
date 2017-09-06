# nginx

#src='/usr/local/src'
src='/home/xue/programs/nginx'
./configure --prefix=/usr/local/nginx  --with-http_ssl_module --add-module=$src/nginx_tcp_proxy_module-master --with-http_gzip_static_module --add-module=$src/ngx_devel_kit  --add-module=$src/lua-nginx-module

make

make install
