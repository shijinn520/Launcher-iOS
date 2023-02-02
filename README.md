# 仅限学习与交流，请勿用在以任何形式（如捐赠，分摊成本，购买兑换码等）的商业行为的私服，如侵权请联系删除侵权内容
支持3.3 3.4 iOS客户端的资源热下载,及游戏内下载资源，不用再去拷贝文件(目前仍然支持老版本的资源热下载)
你也可以在你的GC中接入，需要修改list
iOS3.4：[前往下载](https://oss.mihoyu.cn/d/Onedrive/GenshinImpact/GenshinImpactGC3.4.0.ipa)
# 使用方法-仅支持https协议的服务器
下载安装小火箭-安装并信任小火箭证书-开启https解密-添加以下模块

```RE
#!name=代理模块

[URL Rewrite]
^https:\/\/([\da-z\-\.]+)\.hoyoverse\.com https://sdk.mihoyu.cn header
^https:\/\/([\da-z\-\.]+)\.mihoyo\.com https://sdk.mihoyu.cn header
[MITM]
hostname = %APPEND% *.hoyoverse.com,*.mihoyo.com
```

然后全局路由修改为代理-开启udp转发-开启小火箭-进入游戏下载资源

# 下载完资源后切换至自定义服务器
修改模块中的-sdk.mihoyu.cn-

如我要连接https://yuanshen.com服务器，只需要将模块修改为：

```RE
#!name=代理模块

[URL Rewrite]
^https:\/\/([\da-z\-\.]+)\.hoyoverse\.com https://yuanshen.com header
^https:\/\/([\da-z\-\.]+)\.mihoyo\.com https://yuanshen.com header
[MITM]
hostname = %APPEND% *.hoyoverse.com,*.mihoyo.com
```

即可

# 关于其他方法自行研究
# 此存储库仅供学习交流，有人干坏事不关我事，如侵权可联系删除
