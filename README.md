## 1.下载nginx源码包并解压
  http://nginx.org/en/download.html下载.tar.gz的源码包
## 2.安装依赖包
　yum install openssl-devel pcre-devel zlib-devel
## 3.为nginx设置安装目录
  去到解压目录，运行 ./configure --prefix=/installDir --with-http_ssl_module --with-http_flv_module --with-http_gzip_static_module
### 所有选项
  ./configure \n
　　　　　　--prefix=/installDir \n
           --sbin-path=/
           --conf-path=/etc/nginx/nginx.conf  \n
           --error-log-path=/var/log/nginx/error.log  \n
           --pid-path=/var/run/nginx/nginx.pid  \n
           --lock-path=/var/lock/nginx.lock  \n
           --user=nginx  \n
           --group=nginx  \n
           --with-http_ssl_module  \n
           --with-http_flv_module  \n
           --with-http_gzip_static_module  \n
           --http-log-path=/var/log/nginx/access.log  \n
           --http-client-body-temp-path=/var/tmp/nginx/client/  \n
           --http-proxy-temp-path=/var/tmp/nginx/proxy/  \n
           --http-fastcgi-temp-path=/var/tmp/nginx/fcgi/  \n
