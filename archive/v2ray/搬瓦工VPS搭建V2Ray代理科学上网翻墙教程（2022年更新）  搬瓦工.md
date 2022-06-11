[搬瓦工VPS搭建V2Ray代理科学上网翻墙教程（2022年更新） | 搬瓦工](https://bwgvps.github.io/build-v2ray-on-bandwagonhost-vps/)

大部分国内用户购买搬瓦工VPS都是用于翻墙的，但是很多朋友在买了搬瓦工VPS并不知道如何搭建代理，今天就以目前最火也是最稳的代理方式V2Ray为例，从零开始介绍搬瓦工VPS如何搭建V2Ray代理实现科学上网翻墙。

第一步自然是购买搬瓦工VPS，一般来说，推荐大家购买搬瓦工CN2 GIA（美国CN2 GIA）套餐，三网CN2 GIA线路，国内访问速度快，晚高峰也不卡顿，季付49.99美元起，国内体验非常不错。如果你预算不够，则购买搬瓦工CN2 GT（美国CN2 GT）套餐，线路质量没有CN2 GIA好，但是国内速度也比非优化线路要好，年付49.99美元起。最后，如果你预算很多，那么直接购买搬瓦工香港CN2 GIA，香港线路，三网直连，低延迟、速度快。

本站推荐的搬瓦工套餐如下：

| 套餐 | CPU | 内存 | 硬盘 | 宽带 | 流量/月 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 美国CN2 GT | 1核 | 1GB | 20G | 1Gbps | 1TB | _$49.99/年_ | [立即购买](https://linknn.net/bwg/57) |
| 美国CN2 GIA | 2核 | 1GB | 20G | 2.5Gbps | 1TB | $49.99/季度$169.99/年 | [立即购买](https://linknn.net/bwg/87) |
| 香港CN2 GIA | 2核 | 2GB | 40G | 1Gbps | 500GB | $89.99/月$899.99/年 | [立即购买](https://linknn.net/bwg/95) |

详细的搬瓦工注册与购买教程可以参考[搬瓦工注册与购买教程，循环优惠码，支持支付宝付款](https://bwgvps.github.io/purchase-bandwagonhost/)

## [](https://bwgvps.github.io/build-v2ray-on-bandwagonhost-vps/#%E8%BF%9E%E6%8E%A5%E6%90%AC%E7%93%A6%E5%B7%A5VPS "连接搬瓦工VPS")连接搬瓦工VPS

买好搬瓦工VPS后，搬瓦工会将VPS的连接信息发到你的注册邮箱，root密码可以在KiwiVM控制面板查看，详细教程可以参考[搬瓦工SSH连接信息查看：IP、端口、密码](https://bwgvps.github.io/bandwagonhost-vps-info/)

找到连接信息后，就是在本地连接搬瓦工VPS了，_Windows用户可以使用PuTTY，Mac用户可以使用自带的终端。_

**Windows连接搬瓦工VPS**：

![填写SSH信息.png](https://i.loli.net/2021/07/19/V54iS93KJkF8oGb.png)

**Mac连接搬瓦工VPS**：

![Terminal命令.jpg](https://i.loli.net/2021/07/19/8jBafbPVnuMpgNt.jpg)

详细图文教程：[本地Windows/Mac连接搬瓦工VPS教程](https://bwgvps.github.io/connect-bandwagonhost-vps/)

## [](https://bwgvps.github.io/build-v2ray-on-bandwagonhost-vps/#%E6%90%AD%E5%BB%BAV2Ray%E4%BB%A3%E7%90%86 "搭建V2Ray代理")搭建V2Ray代理

目前，已经成功购买搬瓦工VPS，并且成功连上搬瓦工VPS了。

输入下面命令安装V2Ray：

<table><tbody><tr><td><pre><span>1</span><br></pre></td><td><pre><span>bash &lt;(curl -s -L https://git.io/bwg_v2ray)</span><br></pre></td></tr></tbody></table>

这里如果提示`curl: command not found`，则先安装curl：

-   Ubuntu/Debian系统安装curl方法: `apt-get update -y && apt-get install curl -y`
-   CentOS系统安装curl方法: `yum update -y && yum install curl -y`

安装好curl后再次运行`bash <(curl -s -L https://git.io/bwg_v2ray)`即可。

第一步是提示安装还是卸载，自然是开始安装，输入1即可开始安装：

![v2ray-install.png](https://i.loli.net/2021/08/05/LOAWaQhzGoDNBnY.png)

之后是选择V2Ray传输协议，很多种，包括TCP、WebSocket等，如果你不知道怎么选就直接回车选择默认的TCP即可：

![v2ray-protocol-option.png](https://i.loli.net/2021/08/05/gkBQqrY1lG5ZD9a.png)

接下来就是一些其他设置，如V2Ray端口、是否开启广告拦截、是否配置Shadowsocks等，一样的，如果你不知道怎么选就直接回车选择默认的即可：

![v2ray-other-options.png](https://i.loli.net/2021/08/05/F3vdb9pfMUgytwH.png)

选完配置后，就到了最后一步，确认无误后按下回车键开始安装V2Ray：

![v2ray-install-start.png](https://i.loli.net/2021/08/05/sihXO562mdDuFfR.png)

最后，如下图所示，就表示你的搬瓦工VPS成功安装V2Ray了，页面上显示的是你V2Ray的连接信息：

![v2ray-install-end.png](https://i.loli.net/2021/08/05/KV9tenqiwbPG7Ak.png)

配置文件路径：

-   V2Ray 配置文件路径：/etc/v2ray/config.json
-   Caddy 配置文件路径：/etc/caddy/Caddyfile
-   脚本配置文件路径: /etc/v2ray/233blog\_v2ray\_backup.conf

## [](https://bwgvps.github.io/build-v2ray-on-bandwagonhost-vps/#%E7%AE%A1%E7%90%86V2Ray%E4%BB%A3%E7%90%86 "管理V2Ray代理")管理V2Ray代理

成功安装V2Ray后，我们直接输入`v2ray`即可打开管理页面，如下图：

![v2ray-manage.png](https://i.loli.net/2021/08/05/2W4vXpLy8mfUNYA.png)

常见的管理命令如下：

-   `v2ray info` 查看 V2Ray 配置信息
-   `v2ray config` 修改 V2Ray 配置
-   `v2ray link` 生成 V2Ray 配置文件链接
-   `v2ray infolink` 生成 V2Ray 配置信息链接
-   `v2ray qr` 生成 V2Ray 配置二维码链接
-   `v2ray ss` 修改 Shadowsocks 配置
-   `v2ray ssinfo` 查看 Shadowsocks 配置信息
-   `v2ray ssqr` 生成 Shadowsocks 配置二维码链接
-   `v2ray status` 查看 V2Ray 运行状态
-   `v2ray start` 启动 V2Ray
-   `v2ray stop` 停止 V2Ray
-   `v2ray restart` 重启 V2Ray
-   `v2ray log` 查看 V2Ray 运行日志
-   `v2ray update` 更新 V2Ray
-   `v2ray update.sh` 更新 V2Ray 管理脚本
-   `v2ray uninstall` 卸载 V2Ray

## [](https://bwgvps.github.io/build-v2ray-on-bandwagonhost-vps/#%E9%85%8D%E7%BD%AEV2Ray%E5%AE%A2%E6%88%B7%E7%AB%AF "配置V2Ray客户端")配置V2Ray客户端

完成V2Ray服务端搭建后，我们就需要在本地客户端配置V2Ray了，支持iOS、Android手机、Mac、Windows等，其实就是在客户端上填入上一步的连接信息即可。

详细教程整理如下。

**1、iOS苹果手机客户端**

[iOS苹果手机客户端Shadowrocket下载方法与使用教程](https://github.com/bwgvps/v2ray-tutorial/wiki/iOS%E8%8B%B9%E6%9E%9C%E6%89%8B%E6%9C%BA%E5%AE%A2%E6%88%B7%E7%AB%AFShadowrocket%E4%B8%8B%E8%BD%BD%E6%96%B9%E6%B3%95%E4%B8%8E%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)

**2、Android安卓手机客户端**

[安卓手机客户端v2rayNG下载方法与使用教程](https://github.com/bwgvps/v2ray-tutorial/wiki/%E5%AE%89%E5%8D%93%E6%89%8B%E6%9C%BA%E5%AE%A2%E6%88%B7%E7%AB%AFv2rayNG%E4%B8%8B%E8%BD%BD%E6%96%B9%E6%B3%95%E4%B8%8E%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)

**3、Mac客户端**

[Mac客户端V2RayX下载方法与使用教程](https://github.com/bwgvps/v2ray-tutorial/wiki/Mac%E5%AE%A2%E6%88%B7%E7%AB%AFV2RayX%E4%B8%8B%E8%BD%BD%E6%96%B9%E6%B3%95%E4%B8%8E%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)

**4、Windows客户端**

[Windows客户端v2rayN下载方法与使用教程](https://github.com/bwgvps/v2ray-tutorial/wiki/Windows%E5%AE%A2%E6%88%B7%E7%AB%AFv2rayN%E4%B8%8B%E8%BD%BD%E6%96%B9%E6%B3%95%E4%B8%8E%E4%BD%BF%E7%94%A8%E6%95%99%E7%A8%8B)

## [](https://bwgvps.github.io/build-v2ray-on-bandwagonhost-vps/#%E6%90%AD%E5%BB%BAV2Ray%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98 "搭建V2Ray常见问题")搭建V2Ray常见问题

这个V2Ray一键脚本支持：

1.  支持 V2Ray 多数传输协议
2.  支持 WebSocket + TLS / HTTP/2
3.  支持 动态端口 (WebSocket + TLS，Socks5， HTTP/2 除外)
4.  支持 屏蔽广告
5.  支持 配置 Shadowsocks
6.  支持 下载客户端配置文件 (不用 Xshell 也可以下载)
7.  客户端配置文件同时支持 SOCKS 和 HTTP
8.  支持 生成 V2Ray 配置二维码链接 (仅适用部分客户端)
9.  支持 生成 V2Ray 配置信息链接
10.  支持 生成 Shadowsocks 配置二维码链接
11.  支持修改 V2Ray 传输协议
12.  支持修改 V2Ray 端口
13.  支持修改 动态端口
14.  支持修改 用户ID
15.  支持修改 TLS 域名
16.  支持修改 Shadowsocks 端口
17.  支持修改 Shadowsocks 密码
18.  支持修改 Shadowsocks 加密协议
19.  自动启用 BBR 优化 (如果内核支持)
20.  集成可选安装 BBR (by teddysun.com)
21.  集成可选安装 锐速 (by moeclub.org)
22.  一键 查看运行状态 / 查看配置信息 / 启动 / 停止 / 重启 / 更新 / 卸载 / 等等…
23.  人性化向导 & 纯净安装 & 卸载彻底

在使用过程中一般不会出现问题，直接选择下一步就可以了，如果你的系统不支持使用这个脚本，可以尝试更换一个系统，支持Ubuntu 16+ / Debian 8+ / CentOS 7+，推荐使用 Debian 9 系统，脚本会自动启用 BBR 优化。
