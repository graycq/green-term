# Cloudflare-workers/pages代理脚本
### 本项目仅支持本地化部署
### 本项目不使用订阅器、节点转换等第三方外链引用，无需担心节点订阅被外链作者查看
--------------------------------
## 脚本特色：
### 懒人小白专用！默认节点都为CF官方IP，无需频繁更新订阅获取客户端优选IP
#### Workers方式：支持vless+ws+tls、trojan+ws+tls、vless+ws、trojan+ws代理节点
#### Pages方式：支持vless+ws+tls、trojan+ws+tls代理节点
#### CF Vless/Trojan的单节点支持path路径自定义三类proxyip（IPV4形式、IPV6形式、域名形式）
#### 支持单节点链接、聚合通用节点订阅、sing-box节点订阅、clash节点订阅
### 目前CF Vless/Trojan分为混淆版与未混淆版，两者无区别，都可使用
-------------------------------------------------------------



### 2、VPS专用：

推荐使用 离中国近、便宜、流量多的纯IPV6的vps进行搭建。近可能避免使用IPV4，因为IPV4大概率被大佬们偷扫反代IP，成为他们的公益或收费反代IP库。如果非要用IPV4，请时常关注下自己VPS的流量，使用proxyip与客户端优选IP都会消耗VPS流量

搭建proxyip与反代ip的脚本推荐：[x-ui-yg脚本](https://github.com/yonggekkk/x-ui-yg)、[sing-box-yg脚本](https://github.com/yonggekkk/sing-box-yg)

相关操作请看[视频教程高阶1](https://youtu.be/QOnMVULADko)、[视频教程高阶2](https://youtu.be/CVZStM0t8BA)

### 3、可现实以下四种情况(推荐在TLS节点环境下)：

可选择现实1：仅用于客户端优选IP，即CF节点访问非CF网站的落地IP地区与VPS地区一致，访问CF网站落地IP地区根据proxyip决定

可选择现实2：仅用于proxyip，即CF节点访问CF网站的落地IP地区与VPS地区一致，访问非CF网站落地IP地区根据客户端优选IP决定

可选择现实3：同时用于客户端优选IP与proxyip，即CF节点访问CF网站的落地IP地区、访问非CF网站落地IP地区，两者都与VPS地区一致

可选择现实4：通过在VPS安装WARP全局双栈V4+V6功能，即访问非CF网站的客户端优选IP的落地IP（104.28……/2a09:……）现实固定，或访问CF网站的proxyip的落地IP（104.28……/2a09:……）现实WARP解锁功能效果

---------------------------------

## 五：查看配置信息与分享链接

CF Vless：在网页地址栏输入 https:// workers域名 或者 pages域名 或者 自定义域名 /自定义uuid

CF Trojan：在网页地址栏输入 https:// workers域名 或者 pages域名 或者 自定义域名 /自定义密码

注意：

1、workers域名 或者 pages域名 或者 自定义域名如果都被墙，必须开代理才能打开

2、使用自定域时，原先workers域名 或者 pages域名下的配置信息与分享链接依旧可用

---------------------------------



## 七：客户端推荐

#### 启用分片(Fragment)功能的好处：无视域名被墙TLS阻断，从而让workers等被墙的域名支持TLS节点
#### 提示：未被墙TLS阻断的自定义域名或pages域名无需开启分片就可使用TLS节点
 
目前支持该功能的平台客户端如下（点击名称即跳转到官方下载地址）

1、安卓Android：[v2rayNG](https://github.com/2dust/v2rayNG/tags)、[Nekobox](https://github.com/maskedeken/NekoBoxForAndroid/tags)、[Karing](https://github.com/KaringX/karing/tags)、v2box

2、电脑Windows：[v2rayN](https://github.com/2dust/v2rayN/tags)、[Hiddify](https://github.com/hiddify/hiddify-next/tags)、[Karing](https://github.com/KaringX/karing/tags)

3、苹果Ios：Karing、Hiddify Proxy & VPN、Shadowrocket(小火箭)、Streisand、v2box

4、软路由Openwrt：[homeproxy](https://github.com/kiddin9/openwrt-packages)，建议使用系统自带的软件库查找更新

注意：其他平台客户端未开启分片功能情况下，workers域的6个443系TLS节点是不可用的

注意：Shadowrocket(小火箭)、v2box、v2rayn、v2rayng客户端对trojan+ws有强制开启TLS问题，造成trojan+ws不通。且clash订阅没有trojan+ws节点。特此说明

---------------------------------

### 相关说明及注意点请查看[甬哥博客](https://ygkkk.blogspot.com/2023/07/cfworkers-vless.html)

### 视频教程：

[CF workers永久免费vless节点搭建教程（一）：全网首发演示跳IP现象，解密两大节点使用技巧，优选IP、优选域名的优缺点说明](https://youtu.be/9V9CQxmfwoA)

[CF workers永久免费vless节点搭建教程（二）：优选反代IP一键脚本发布，pages部署教程，多平台客户端设置说明，独家探讨CF免费代理敏感安全问题](https://youtu.be/McdRoLZeTqg)

[CF workers永久免费Trojan节点搭建教程（三）：无需自定义域名，workers与pages两方案部署优选IP节点；CF Trojan与CF Vless对比总结；如何看待Trojan被识别](https://youtu.be/lmhhL8M1k0I)

强烈推荐：[CF vless/trojan永久免费节点教程（四）：解读优选官方IP、优选反代IP、优选域名三者的关系与特点；ProxyIP存在的意义](https://youtu.be/NaLd-orwFUE)

强烈推荐：[CF vless/trojan永久免费节点教程（五）：不用自定义域名？不用频繁优选IP？不用订阅器？总结CF节点与域名的结构关系图](https://youtu.be/8s-ELRuFaeE)

强烈推荐：[CF vless/trojan永久免费节点教程（六）：节点不能用，问题出在哪？多平台免费客户端设置指南及避坑说明](https://youtu.be/8E0l0nQWLxs)

高阶推荐：[CF vless/trojan永久免费节点最终教程（七）：全网独家演示真正的"固定IP"，解决twitch、chatgpt客户端报错问题；一键自制反代IP与ProxyIP；揭秘你被他人偷扫IP的风险](https://youtu.be/QOnMVULADko)

高阶推荐：[CF vless/trojan永久免费节点最终教程（八）：自建全端口通用的ProxyIP，同时支持客户端地址优选反代IP，自建反代IP的最终教程](https://youtu.be/CVZStM0t8BA)

[直播精选回顾：CF workers vless免费节点四大特点，节点被断流阻断问题](https://youtu.be/9OHGpWlfdJ0)

[ClouDNS永久免费域名最终教程：CF pages vless自定义域名直接部署](https://youtu.be/PN0BLANXh4I)

小白优选IP应用推荐：[CF优选IP解放小白最终方案：一键自动生成美国、香港、欧洲三区优选官方IP，电脑WIN、安卓android、苹果ios多平台一键通用](https://youtu.be/6kKIzObEZ2c)

---------------------------------
---------------------------------
---------------------------------
---------------------------------
## 优选域名、优选官方IP+反代IP一键脚本（在本地网络环境下利用termux或者ish运行）：

1、安卓请使用termux官方项目下载客户端（谷歌商店下载的不可用！）：https://github.com/termux/termux-app/releases/tag/v0.118.1

首次安装后，请先安装依赖：```pkg upgrade```，然后运行以下你要使用的脚本

2、苹果手机用户，由于ISH最新版有BUG导致脚本运行卡住，请使用ISH_1.2.2版本，可以用巨魔先安装再降级，网上也有其它指定旧版IPA安装的教程

首次安装后，请先安装依赖：```apk add curl bash```，然后运行以下你要使用的脚本

-------------------------------------------------------------
### 脚本1：CF-优选官方IP (默认美、亚、欧三地区 强烈推荐！！！)，安卓苹果手机平板专用：
```
curl -sSL https://ghp.ci/https://raw.githubusercontent.com/yonggekkk/Cloudflare_vless_trojan/main/cf/cf.sh -o cf.sh && chmod +x cf.sh && bash cf.sh
```
-------------------------------------------------------------

### 脚本2：CF-CDN优选公共大厂域名脚本，苹果安卓手机平板专用：
```
curl -sSL https://gitlab.com/rwkgyg/CFwarp/raw/main/point/CFcdnym.sh -o CFcdnym.sh && chmod +x CFcdnym.sh && bash CFcdnym.sh
```
------------------------------------------------------------------------
### 脚本3：CF-优选官方IP+反代IP二合一脚本（带测速），苹果安卓手机平板专用：
```
curl -sSL https://gitlab.com/rwkgyg/CFwarp/raw/main/point/cfip.sh -o cfip.sh && chmod +x cfip.sh && bash cfip.sh
```
