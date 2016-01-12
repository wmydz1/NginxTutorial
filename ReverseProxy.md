## Reverse Proxy
(反向代理)

```
server {listen 80;server_name xxx123.tk; location / {proxy_redirect off;proxy_set_header Host $host;proxy_set_header X-Real-IP $remote_addr;proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for; proxy_pass http://192.168.10.38:3000;}access_log logs/xxx123.tk_access.log; }server {listen 80;server_name xxx456.tk; location / {proxy_redirect off;proxy_set_header Host $host;proxy_set_header X-Real-IP $remote_addr;proxy_set_header X-Forwarded-For  $proxy_add_x_forwarded_for; 
proxy_pass http://192.168.10.40:80;}access_log logs/xxx456.tk_access.log; }


```

重新加载 nginx 配置文件,使之修改生效,再把 xxx123.tk 域名指向公司静态 IP,这样就成功的做到了在浏览器  
中输入 xxx123.tk 的时候访问的内网服务器 192.168.10.38 的 3000 端口,输入 xxx456.tk 访问 192.168.10.40 的 80 端口的作用。  
