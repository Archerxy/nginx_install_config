## 1.下载nginx源码包并解压
  http://nginx.org/en/download.html下载.tar.gz的源码包
## 2.安装依赖包
　yum install openssl-devel pcre-devel zlib-devel
## 3.为nginx设置安装目录
  去到解压目录，运行 ./configure --prefix=/installDir --with-http_ssl_module --with-http_flv_module --with-http_gzip_static_module
#### 所有配置选项
  ./configure   
  --prefix=/installDir   
  --sbin-path=/  
  --conf-path=/etc/nginx/nginx.conf    
  --error-log-path=/var/log/nginx/error.log   
  --pid-path=/var/run/nginx/nginx.pid   
  --lock-path=/var/lock/nginx.lock   
  --user=nginx   
  --group=nginx   
  --with-http_ssl_module   
  --with-http_flv_module   
  --with-http_gzip_static_module   
  --http-log-path=/var/log/nginx/access.log   
  --http-client-body-temp-path=/var/tmp/nginx/client/   
  --http-proxy-temp-path=/var/tmp/nginx/proxy/   
  --http-fastcgi-temp-path=/var/tmp/nginx/fcgi/   
