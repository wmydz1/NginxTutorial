
```
./configure --with-http_ssl_module \
      --with-http_v2_module \
      --with-debug \
      --with-openssl=../openssl-1.0.2e
      
```

```

./configure --user=www --group=www  --prefix=/usr/local/nginx --with- 
pcre --with-http_ssl_module --with-http_realip_module --with- 
http_addition_module --with-http_sub_module --with-http_dav_module --  
with-http_flv_module --with-http_mp4_module --with-http_gunzip_module --  
with-http_gzip_static_module --with-http_random_index_module --with-  
http_secure_link_module --with-http_stub_status_module --with-mail --  
with-mail_ssl_module --with-ipv6  


```

- 1、 Tar:解压这个源码软件包。- 2、 Cd:进入到这个源码包。- 3、 ./configure:“configure”会在你的系统上测试存在的特性(或者bug!)然后来建立  
 Makefile文件来完成make!  - 4、 Make:编译程序。5、 Make install:安装文件!
----
``` 
--prefix=<path> - Nginx安装路径。如果没有指定，默认为 /usr/local/nginx。   
    
 --conf-path=<path> - 在没有给定-c选项下默认的nginx.conf的路径。如果没有指定，默认为<prefix>/conf/nginx.conf。   
    
 --pid-path=<path> - 在nginx.conf中没有指定pid指令的情况下，默认的nginx.pid的路径。如果没有指定，默认为 <prefix>/logs/nginx.pid。   
    
 --lock-path=<path> - nginx.lock文件的路径。   
    
 --error-log-path=<path> - 在nginx.conf中没有指定error_log指令的情况下，默认的错误日志的路径。如果没有指定，默认为 <prefix>/logs/error.log。   
    
 --http-log-path=<path> - 在nginx.conf中没有指定access_log指令的情况下，默认的访问日志的路径。如果没有指定，默认为 <prefix>/logs/access.log。   
    
 --user=<user> - 在nginx.conf中没有指定user指令的情况下，默认的nginx使用的用户。如果没有指定，默认为 nobody。   
    
 --group=<group> - 在nginx.conf中没有指定user指令的情况下，默认的nginx使用的组。如果没有指定，默认为 nobody。   
    
 --with-http_ssl_module -开启HTTP SSL模块，使NGINX可以支持HTTPS请求。需要安装了OPENSSL   
    
 --with-http_flv_module   
    
 --with-http_stub_status_module - 启用 "server status" 页(可有可无)   
    
 --without-http_gzip_module - 禁用 ngx_http_gzip_module. 如果启用，需要 zlib 。   
    
 --without-http_ssi_module - 禁用 ngx_http_ssi_module   
    
 --without-http_referer_module - 禁用 ngx_http_referer_module   
    
 --without-http_rewrite_module - 禁用 ngx_http_rewrite_module. 如果启用需要 PCRE 。   
    
 --without-http_proxy_module - 禁用 ngx_http_proxy_module   
    
 --without-http_fastcgi_module - 禁用 ngx_http_fastcgi_module   
    
 --without-http_memcached_module - 禁用 ngx_http_memcached_module   
    
 --without-http_browser_module - 禁用 ngx_http_browser_module   
    
 --http-proxy-temp-path=PATH - Set path to the http proxy temporary files   
    
 --http-fastcgi-temp-path=PATH - Set path to the http fastcgi temporary files   
    
 --without-http - 禁用 HTTP server（用作代理或反向代理）   
    
 --with-mail - 启用 IMAP4/POP3/SMTP 代理模块   
    
 --with-mail_ssl_module - 启用 ngx_mail_ssl_module   
    
 --with-openssl=DIR - Set path to OpenSSL library sources   
 
 ```  
 
 ----  
 
 
 查看启动状态
   # netstat -tnlp  | grep nginx