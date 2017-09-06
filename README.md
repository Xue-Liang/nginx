# nginx

#src='/usr/local/src'

src='/home/xue/programs/nginx'

#prefix=/usr/local/nginx

prefix=/home/xue/programs/nginx

./configure --prefix=/usr/local/nginx  --with-http_ssl_module --add-module=$src/nginx_tcp_proxy_module-master --with-http_gzip_static_module --add-module=$src/ngx_devel_kit  --add-module=$src/lua-nginx-module

make

make install

/**

http://openresty.org/cn/dynamic-routing-based-on-redis.html

step 1.下载如下插件

https://codeload.github.com/openresty/lua-redis-parser/tar.gz/v0.13

https://codeload.github.com/openresty/lua-nginx-module/tar.gz/v0.10.10

https://codeload.github.com/openresty/redis2-nginx-module/tar.gz/v0.14

https://codeload.github.com/simpl/ngx_devel_kit/tar.gz/v0.3.0

https://codeload.github.com/openresty/set-misc-nginx-module/tar.gz/v0.31

*/
