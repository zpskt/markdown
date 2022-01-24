# markdown
利用nodejs的docsify实现一个简单的web程序，用markdown作为页面内容
## 来源视频
[CodeSheep](https://www.bilibili.com/video/BV1eu411m797?spm_id_from=333.1007.top_right_bar_window_history.content.click)
## 教程
解压simpleweb.zip
### 自己新建一个web  
要求：nodejs环境  
安装docsify

    cnpm install -g docsify-cli
新建你的目录文件夹，进入

    mkdir src && cd src
初始化 docsify，选择yes
docsify init
>zp@zp src % docsify init  
. already exists.  
✔ Are you sure you want to rewrite it? (y/N) true  
Initialization succeeded! Please run docsify serve

你可以用docsify serve运行一下  

    docsify serve
默认在本机http://localhost:3000

src文件夹里会出现README.md文件，md文件被渲染成html内容.
### 安装nginx（略）
### nginx设置
修改nginx配置文件
>        location / {
>            root   /usr/local/nginx/www/src;#这里是你的文件夹存放地址
>           index  index.html index.htm;
>        }

开启nginx

    /usr/local/nginx/sbin/nginx 

重启nginx（修改配置文件后)
   
    /usr/local/nginx/sbin/nginx -s reload