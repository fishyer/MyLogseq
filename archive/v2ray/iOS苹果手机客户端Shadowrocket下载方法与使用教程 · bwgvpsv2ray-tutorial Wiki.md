[iOS苹果手机客户端Shadowrocket下载方法与使用教程 · bwgvps/v2ray-tutorial Wiki](https://github.com/bwgvps/v2ray-tutorial/wiki/iOS%E8%8B%B9%E6%9E%9C%E6%89%8B%E6%9C%BA%E5%AE%A2%E6%88%B7%E7%AB%AFShadowrocket%E4%B8%8B%E8%BD%BD%E6%96%B9%E6%B3%95%E4%B8%8E%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)

Shadowrocket，又名小火箭，是iOS苹果手机上用的最多的一款代理软件，支持Shadowsocks、V2Ray、Trojan等，并且Shadowrocket更新也非常及时。本文介绍Shadowrocket下载方法和Shadowrocket使用教程。

## Shadowrocket 下载

由于一些原因，App Store中国大陆地区已下架所有VPN应用，包括Shadowrocket，一般来说，国内用户想要下载Shadowrocket，有以下两种解决方案。

解决方案

1.申请国外地区AppleID(推荐)或者某宝购买，使用他人的AppleID 一定不要开iCloud同步。

2.手机越狱(不推荐)

## Shadowrocket 使用教程

首要的就是进行客户端配置，可以选择二维码导入或者手动填写。

今天主要以手动填写(Vmess)为例，给出详细的教程。

先选择手动填写(Vmess)，会弹出一个界面，如下图所示（**只有TLS+websocket模式时才需要配置TLS和websocket，否者直接默认即可**）：

![配置 1.png](https://camo.githubusercontent.com/1a8f56e4e858ea4debc035084052367e32089d0455c27a18855593a41fe4411c/68747470733a2f2f692e6c6f6c692e6e65742f323032312f30382f30332f6270573172346449515877394776612e706e67)

接着我们需要在该页面中填一些信息:

1.地址 端口和UUID(ID) 对应填写

2.算法,选择自动

3.TLS+websocket模式时，打开TLS 允许不安全，混淆选择websocket 配置path和host

4.其他默认即可

确认信息填写无误后，点击右上角"完成",进行保存。

完成后，我们就可以自如的连接上网了。
