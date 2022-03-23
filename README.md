# use_clash_in_linux

在linux虚拟机中用clash翻墙的笔记。

## 下载

### 下载clash

找一个你喜欢的路径下载clash，

<https://github.com/Dreamacro/clash/releases>

### 下载config.yaml

进入~/.config/clash/路径下，

```
wget -O config.yaml 你的clash的订阅地址
```

也可以把windows上的yaml文件复制过来，改个名字。clash for windows，profiles，右击正在使用的那个yaml文件，show in folder，就可以找到；路径一般是C:\Users\xxx\\.config\clash\profiles。

Glados提供的网址如下（似乎已失效），

```
wget -O config.yaml https://update.glados-config.net/clash/73020/ac2a3dc/25084/glados_new.yaml
```

### 下载Country.mmdb

进入~/.config/clash/路径下，

```
wget -O Country.mmdb https://www.sub-speeder.com/client-download/Country.mmdb
```

## 配置

解压、运行clash。

登录<http://clash.razord.top/#/proxies>可以管理clash配置。

打开设置，进入network，选network proxy，选择manual，将http proxy和socks host的端口填写成在web管理页面中配置的那个，IP填127.0.0.1。

然后就可以愉快上网了。

## 使用 proxychain

用 apt install 安装 proxychain；

修改 /etc/proxychains.conf，在最后加入一行： socks5 物理机IP 端口(一般为7890)；

开启物理机上 clash 的允许局域网连接选项，代理模式改为全局；

在需要代理的指令前加 proxychains。

## 我的环境

ubuntu18虚拟机。

## 参考

<http://www.ptbird.cn/ubuntu-2004-clash-for-linux.html>

<https://www.jianshu.com/p/acdda87d77e4>

<https://zhuanlan.zhihu.com/p/366589407>

<https://blog.51cto.com/u_15075508/3634165>