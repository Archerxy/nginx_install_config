## 1.下载nginx源码包并解压
  http://nginx.org/en/download.html 下载.tar.gz的源码包
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
  
  
## 缺少opensll库报错时
  1.运行 yum -y install openssl-devel 安装该库   
  2.若安装了该库还是报错说缺少该库，此时需要在后面加上 --with-openssl=/usr/local/bin/openssl  
    这里/usr/local/bin/openssl  可根据 whereis openssl 找到该库的位置
    
## 安装时报错
  make[1]: *** [/usr/local/bin/openssl/.openssl/include/openssl/ssl.h] Error 1   
  make[1]: Leaving directory `/usr/software/nginx-1.18.0'   
  make: *** [build] Error 2   
  这里是因为 openssl 版本不对，需要旧版本 1.0.1版  
  运行 wget https://www.openssl.org/source/old/1.0.1/openssl-1.0.1o.tar.gz  
  解压，安装到指定目录   
  去到nginx解压包目录下运行   
  ./configure --prefix=/installDir --with-http_ssl_module --with-http_flv_module --with-http_gzip_static_module --with-openssl=/usr/local/openssl-1.0.1o

