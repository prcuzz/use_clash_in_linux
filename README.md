# use_clash_in_linux

在linux中用clash翻墙的笔记。

## 下载

### 下载clash

<https://github.com/Dreamacro/clash/releases>

### 下载config.yaml

```
wget -O config.yaml https://update.glados-config.net/clash/73020/ac2a3dc/25084/glados_new.yaml
```

### 下载Country.mmdb

```
wget -O Country.mmdb https://www.sub-speeder.com/client-download/Country.mmdb
```

## 配置

将Country.mmdb和config.yaml放到~/.config/clash/下。

解压、运行clash。

登录<http://clash.razord.top/#/proxies>可以管理clash配置。

打开设置，进入network，选network proxy，选择manual，将http proxy和socks host的端口填写成在web管理页面中配置的那个，IP填127.0.0.1。

然后就可以愉快上网了。

## 我的环境

ubuntu18虚拟机。

## 参考

<http://www.ptbird.cn/ubuntu-2004-clash-for-linux.html>

<https://www.jianshu.com/p/acdda87d77e4>

<https://zhuanlan.zhihu.com/p/366589407>