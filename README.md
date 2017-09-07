# nginx

**一、准备工作
/**

step 1.下载lua
http://www.lua.org/ftp/lua-5.3.4.tar.gz

step 1.1 安装 lua,如果发生 readline/readline.h: 没有那个文件或目录 错误,

执行  debian sudo apt install libreadline-dev
      centos yum install libreadline-dev


step 2.需要单独安装 lua-redis-parser-0.13

https://codeload.github.com/openresty/lua-redis-parser/tar.gz/v0.13


参考资料:(http://openresty.org/cn/dynamic-routing-based-on-redis.html)

step 3.下载如下模块

https://codeload.github.com/openresty/lua-nginx-module/tar.gz/v0.10.10

https://codeload.github.com/openresty/redis2-nginx-module/tar.gz/v0.14

https://codeload.github.com/simpl/ngx_devel_kit/tar.gz/v0.3.0

https://codeload.github.com/openresty/set-misc-nginx-module/tar.gz/v0.31

*/

**二、编译nginx生成nginx可执行文件

#src='/usr/local/src'

src='/home/xue/programs/nginx'

#prefix=/usr/local/nginx

prefix=/home/xue/programs/nginx

#./configure --prefix=$prefix  --with-http_ssl_module --add-module=$src/nginx_tcp_proxy_module-master --with-http_gzip_static_module --add-module=$src/ngx_devel_kit  --add-module=$src/lua-nginx-module

./configure --prefix=$prefix --with-http_gzip_static_module --add-module=$src/lua-nginx-module --add-module=$src/ngx_devel_kit --add-module=$src/redis2-nginx-module-0.14 --add-module=$src/set-misc-nginx-module-0.31                              


make

make install


