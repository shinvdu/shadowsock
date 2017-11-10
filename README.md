shadowsock server: 

安装

Debian / Ubuntu:

apt-get install python-pip
pip install shadowsocks
CentOS:

yum install python-setuptools && easy_install pip
pip install shadowsocks

使用:

ssserver -p 8000 -k password -m rc4-md5

放到后台运行

ssserver -p 8000 -k password -m rc4-md5 -d start
ssserver -p 8000 -k password -m rc4-md5 -d stop

使用配置文件
$ vim /etc/shadowsocks.json

{
    "server":"0.0.0.0",
    "server_port":8888,
    "local_port":1080,
    "password":"f36hh0eee0abad",
    "timeout":600,
    "method":"rc4-md5"
}
ssserver -c /etc/shadowsocks.json -d start

--------------------------------------------------------------------------------

监控：supervisor

pip install supervisord
把centos下面的文件到相应位置
centos/supervisord.conf --> /etc/supervisord.conf
centos/supervisord.d/ --> /etc/supervisord.d
centos/supervisord --> /etc/init.d/supervisord

$ chmod +x /etc/init.d/supervisord
$ chkconfig supervisord on
$ service supervisord start 

http://ip:9999

用户名：baby
密码: hibaby

可对进程进行监控

--------------------------------------------------------------------------------


client:

* android 上面使用： 

下载安装应用shadowsocks apk: 

址址： http://blog.sky-city.me/files/shadowsocks.apk


下在这些配置，在打开安装的那个app后，填进去

服务器: 104.236.134.211
远程端口: 8888
本地端口: 1080
密码:  f36hh0eee0abad
加密方法: RC4-MD5

路由，选择 《绕过局域网及中国大陆地址》

UDP转发: 选上

最后在右上角，打开，即可浏览国外被墙网站。


* win & linux 下面使用浏览器

设置浏览器的代理：
127.0.0.1:1080
即可使用


使用chrome下面的一个插件: SwitchyOmega, 再订阅GFWlist, 便可以实现很流畅地浏览所有的网页了。



--------------------------------------------------------------------------------

bhobihiboijobjibobj


bjibjibjibjib