# edgetunnel
A script based on the FaaS provied by Cloudflare Worker


## Cloudflrae pages(alternative method)


# 变量说明
| 变量名 | 示例 | 必填 | 备注 |
|--------|---------|-|-----|-----|
| UUID | `90cd4a77-141a-43c9-991b-08263cfe9c10` |✅| Powershell -NoExit -Command "[guid]::NewGuid()"|  |
| KEY | `token` |❌| 动态UUID秘钥，使用变量`KEY`的时候，将不再启用变量`UUID`|  |
| TIME | `7` |❌| 动态UUID有效时间(单位:天)|  |
| UPTIME | `3` |❌| 动态UUID更新时间(默认:北京时间`3`点更新) |  |
| PROXYIP | `proxyip.fxxk.dedyn.io:443` |❌| 备选作为访问CFCDN站点的代理节点(支持自定义ProxyIP端口, 支持多ProxyIP, ProxyIP之间使用`,`或`换行`作间隔) | |
| SOCKS5  | `user:password@127.0.0.1:1080` |❌| 优先作为访问CFCDN站点的SOCKS5代理(支持多socks5, socks5之间使用`,`或`换行`作间隔) | |
| GO2SOCKS5  | `blog.cmliussss.com`,`*.ip111.cn`,`*google.com` |❌| 设置`SOCKS5`变量之后，可设置强制使用socks5访问名单(`*`可作为通配符，`换行`作多元素间隔) ||
| ADD | `icook.tw:2053#官方优选域名` |❌| 本地优选TLS域名/优选IP(支持多元素之间`,`或`换行`作间隔) ||
| ADDAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressesapi.txt) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) ||
| ADDNOTLS | `icook.hk:8080#官方优选域名` |❌| 本地优选noTLS域名/优选IP(支持多元素之间`,`或`换行`作间隔) ||
| ADDNOTLSAPI | [https://raw.github.../addressesapi.txt](https://raw.githubusercontent.com/cmliu/CFcdnVmess2sub/main/addressesapi.txt) |❌| 优选IP的API地址(支持多元素之间`,`或 换行 作间隔) ||
| ADDCSV | [https://raw.github.../addressescsv.csv](https://raw.githubusercontent.com/cmliu/WorkerVless2sub/main/addressescsv.csv) |❌| iptest测速结果(支持多元素, 元素之间使用`,`作间隔) ||
| DLS | `8` |❌| `ADDCSV`测速结果满足速度下限 ||
| TGTOKEN | `6894123456:XXXXXXXXXX0qExVsBPUhHDAbXXX` |❌| 发送TG通知的机器人token | 
| TGID | `6946912345` |❌| 接收TG通知的账户数字ID | 
| SUB | `VLESS.fxxk.dedyn.io` | ❌ | 内建域名、IP节点信息的订阅生成器地址 ||
| SUBAPI | `SUBAPI.fxxk.dedyn.io` |❌| clash、singbox等 订阅转换后端 | |
| SUBNAME | `edgetunnel` |❌| | |
| RPROXYIP | `false` |❌| 设为 true 即可强制获取订阅器分配的ProxyIP(需订阅器支持)| |
| URL302 | `https://t.me/CMLiussss` |❌| 主页302跳转|  |
| URL | `https://blog.cmliussss.com` |❌| 主页反代伪装|  |
| CFPORTS | `2053`,`2096`,`8443` |❌| CF账户标准端口列表 |  |



# Acknowledgement
[zizifn](https://github.com/zizifn/edgetunnel)、[3Kmfi6HP](https://github.com/6Kmfi6HP/EDtunnel)、[Stanley-baby](https://github.com/Stanley-baby)、[ACL4SSR]
