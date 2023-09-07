# 青少年CTF基础Docker镜像
## 说明
青少年CTF官方的出题基础环境，方便出题人对自己的程序进行构建和打包，并且方便出题人在本地测试。总结、优化了目前多数公开的CTF基础题目镜像，您可以下载后自行修改。

大家如果有好用的镜像或者思路，也可以给我们提供。您可以通过 https://github.com/qsnctf 中的`联系我们`与我们取得联系，并提供您的思路与想法。

**因为镜像过多，并且需要长期维护，也为了方便使用，让大家可以通过`git clone`快速的拉取，然后快速的部署，所以分成了若干个单独的仓库。**

## 镜像列表
- Web
  - 以Nginx为基础的Web镜像
    - Nginx
      - https://github.com/qsnctf/base_nginx
  - 拥有PHP的Nginx镜像
    - Nginx-PHP5.6
      - https://github.com/qsnctf/base_nginx_php_56
    - Nginx-PHP7.2
      - https://github.com/qsnctf/base_nginx_php_72
    - Nginx-PHP7.4
      - https://github.com/qsnctf/base_nginx_php_74
    - Nginx-PHP8.0
      - https://github.com/qsnctf/base_nginx_php_80
  - 拥有PHP和MySQL的Nginx镜像
    - Nginx-PHP5.6-MySQL
      - https://github.com/qsnctf/base_nginx_mysql_php_56
    - Nginx-PHP7.2-MySQL
      - https://github.com/qsnctf/base_nginx_mysql_php_72
    - Nginx-PHP7.4-MySQL
      - https://github.com/qsnctf/base_nginx_mysql_php_74
    - Nginx-PHP8.0-MySQL
      - https://github.com/qsnctf/base_nginx_mysql_php_80
    - 以Apache为基础的Web镜像
      - Apache(httpd)
        - https://github.com/qsnctf/base_httpd
  - 拥有PHP的Apache镜像
    - Apache(httpd)-PHP5.6
      - https://github.com/qsnctf/base_httpd_php_56
    - Apache(httpd)-PHP7.2
      - https://github.com/qsnctf/base_httpd_php_72
    - Apache(httpd)-PHP7.4
      - https://github.com/qsnctf/base_httpd_php_74
    - Apache(httpd)-PHP8.0
      - https://github.com/qsnctf/base_httpd_php_80
  - 拥有PHP和MySQL的Apache镜像
    - Apache(httpd)-PHP5.6-MySQL
      - https://github.com/qsnctf/base_httpd_mysql_php_56
    - Apache(httpd)-PHP7.2-MySQL
      - https://github.com/qsnctf/base_httpd_mysql_php_72
    - Apache(httpd)-PHP7.4-MySQL
      - https://github.com/qsnctf/base_httpd_mysql_php_74
    - Apache(httpd)-PHP8.0-MySQL
      - https://github.com/qsnctf/base_httpd_mysql_php_80
  - 以Python为基础的Web镜像
    - Python2.7
      - https://github.com/qsnctf/base_web_python27
    - Python3.8
      - https://github.com/qsnctf/base_web_python38
    - Python3.10
      - https://github.com/qsnctf/base_web_python310
  - 以Python为基础包含MySQL的Web镜像
    - Python2.7-MySQL
      - https://github.com/qsnctf/base_web_mysql_python27
    - Python3.8-MySQL
      - https://github.com/qsnctf/base_web_mysql_python38
    - Python3.10-MySQL
      - https://github.com/qsnctf/base_web_mysql_python310
- Pwn
  - 以Ubuntu为基础包含Xinetd的Pwn镜像
    - Ubuntu16.04
      - https://github.com/qsnctf/base_pwn_xinetd_ubuntu_1604
    - Ubuntu18.04
      - https://github.com/qsnctf/base_pwn_xinetd_ubuntu_1804
    - Ubuntu20.04
      - https://github.com/qsnctf/base_pwn_xinetd_ubuntu_2004
    - Ubuntu22.04
      - https://github.com/qsnctf/base_pwn_xinetd_ubuntu_2204

- Other
  - 以Python为基础的动态题目脚本镜像
    - https://github.com/qsnctf/base_other_python_http
  - 以Python为基础包含NC的镜像

> 正在努力更新更多的环境...

## 题目投稿
目前仍然采取在论坛提交的方式，可以查看 https://bbs.qsnctf.com/thread-19-1-1.html ,但是建议使用我们目前版本的Web镜像，您如果不会打包Docker镜像，可以只提供源码，并详细说明源码的使用方法和环境配置注意事项。

## 问题反馈
目前仓库中的代码，在发布之前均有测试，如果出现一些问题，您可以在相应仓库的位置提交Issues，如果Issues长时间未处理，可以尝试联系我们。

## 参考与鸣谢


网址：https://github.com/CTF-Archives/ctf-docker-template
> 感谢陈橘墨、探姬人维护的仓库，给出了解决PHP5.6-Apache中因Debian9源镜像站弃用、修改导致的404相关问题的思路。

网址：https://github.com/ctfhub-team/ctfhub_base_image
> 感谢CTFhub的师傅的铺垫，根据上述仓库，我们在Python项目中增加调用了Gunicorn的WSGI，减轻并发压力。
> 
> 同时也感谢CTFHub的师傅给出Ubuntu镜像中TCPDUMP和32位支持。
> 
网址：https://www.fujieace.com/kali-linux/lib32ncurses5.html
> 感谢付杰在付杰博客中提出的`E: Unable to locate package lib32ncurses5`的相关解决方式。因为横跨了多个Ubuntu版本，相关源有所变更。
> 
网址：https://blog.csdn.net/fjh1997/article/details/113405060
> 感谢fjh1997在CSDN发布的`构建ubuntu20 pwn题目镜像出现cp: cannot overwrite non-directory ‘/home/ctf/lib‘ with directory ‘ /usr/lib‘`并指出在Ubunt 19.04以上`/lib*`这个目录中的文件是软连接，来自于`/usr/lib*`

