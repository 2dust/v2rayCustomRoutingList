# v2rayCustomRoutingList

### 文件用途
- proxy:需要代理的Domain或IP
- direct:需要直连的Domain或IP
- block:需要阻止的Domain或IP

### 内容格式
- 纯字符串: 当此字符串匹配目标域名中任意部分，该规则生效。比如"sina.com"可以匹配"sina.com"、"sina.com.cn"和"www.sina.com"，但不匹配"sina.cn"。
- 正则表达式: 由"regexp:"开始，余下部分是一个正则表达式。当此正则表达式匹配目标域名时，该规则生效。例如"regexp:\\.goo.*\\.com$"匹配"www.google.com"、"fonts.googleapis.com"，但不匹配"google.com"。
- 子域名 (推荐): 由"domain:"开始，余下部分是一个域名。当此域名是目标域名或其子域名时，该规则生效。例如"domain:v2ray.com"匹配"www.v2ray.com"、"v2ray.com"，但不匹配"xv2ray.com"。
- 完整匹配: 由"full:"开始，余下部分是一个域名。当此域名完整匹配目标域名时，该规则生效。例如"full:v2ray.com"匹配"v2ray.com"但不匹配"www.v2ray.com"。
- IP: 形如"127.0.0.1"。
- CIDR: 形如"10.0.0.0/8".

### How to use
- 找到自己需要的内容
- 在Issue提交或Pull
- 等待
- 最终在v2rayN和v2rayNG的自定义路由设置中方便使用(还未开发)
