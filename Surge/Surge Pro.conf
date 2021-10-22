# Update-2021.10.18

[General]
# 通用设置

# > 增强版 Wi-Fi 助理
# (在 Wi-Fi 网络不佳时尝试使用数据网络建立连接，请仅当使用不限量的数据流量时开启)
wifi-assist = false

# > Internet 测试 URL
internet-test-url = http://wifi.vivo.com.cn/generate_204

# > 代理测速 URL
proxy-test-url = http://cp.cloudflare.com/generate_204

# > 测试超时（秒）
test-timeout = 5

# > TLS 引擎
tls-provider = openssl

# > 自定义 GeoIP 数据库
geoip-maxmind-url = https://raw.githubusercontent.com/JMVoid/ipip2mmdb/release/Country.mmdb

# > 隐藏状态栏上的VPN图标
hide-vpn-icon = false

# > IPv6 支持（默认关闭）
ipv6 = false

# > 允许 Wi-Fi 访问 (仅 iOS ）
allow-wifi-access = true
wifi-access-http-port = 6152
wifi-access-socks5-port = 6153

# > 允许 Wi-Fi 访问 (仅 macOS，若允许远程访问将「127.0.0.1」改为「0.0.0.0」)
http-listen = 127.0.0.1:6152
socks5-listen = 127.0.0.1:6153

# > HTTP-API
# 依次为：密码，主机名，端口
http-api = Godrock@0.0.0.0:6171

# > HTTP-API-TLS
http-api-tls = false

# > Web控制器
# Safari输入127.0.0.1:6171,填入HTTP-API密码即可。
http-api-web-dashboard = true

# > 兼容模式 (仅 iOS)
# compatibility-mode = 0

# > 跳过代理
skip-proxy = 127.0.0.1, 192.168.0.0/16, 10.0.0.0/8, 172.16.0.0/12, 100.64.0.0/10, localhost, *.local, passenger.t3go.cn

# > 排除简单主机名
exclude-simple-hostnames = true

# > Network framwork
# 启动 Network.framework 以开启用户态网络协议栈，可提高吞吐量，降低延迟并开启 MPTCP。（需手动重启 Surge) 实验性功能可能导致 Surge 不稳定，甚至引起系统崩溃。
# > 默认关闭：false ，可根据自己的需求选择开启：true 。
network-framework = true

# > DNS 服务器
dns-server = 119.29.29.29, 223.5.5.5, 223.6.6.6, system

# > DNS over HTPPS (如无必要不建议使用 DNS over HTTPS)
# doh-server = https://dns.alidns.com/dns-query
# > 从 /etc/hosts 读取 DNS 记录
read-etc-hosts = true

# 高级设置

# > 日志级别
loglevel = warning

# > 当遇到 REJECT 策略时返回错误页
show-error-page-for-reject = true

# > Always Real IP Hosts
always-real-ip = msftconnecttest.com, msftncsi.com, *.msftconnecttest.com, *.msftncsi.com, *.srv.nintendo.net, *.stun.playstation.net, xbox.*.microsoft.com, *.xboxlive.com, *.battlenet.com.cn, *.battlenet.com, *.blzstatic.cn, *.battle.net

# Hijack DNS
# hijack-dns = 8.8.8.8:53, 8.8.4.4:53

# > TCP Force HTTP Hosts
force-http-engine-hosts = *.ott.cibntv.net, 123.59.31.1,119.18.193.135, 122.14.246.33, 175.102.178.52, 116.253.24.*, 175.6.26.*, 220.169.153.*

# > VIF Excluded Routes
tun-excluded-routes = 239.255.255.250/32

# > 路由防火墙
# 包含所有的网络请求
include-all-networks = false

# 包含本地网络请求
include-local-networks = false

[Replica]
# 0 为关闭，1 为开启

# > 隐藏 Apple 请求
hide-apple-request = 0

# > 隐藏崩溃追踪器请求
hide-crash-reporter-request = 1

# > 隐藏 UDP 会话
hide-udp = 0

# > 关键词过滤器
# keyword-filter-type = none

# > 关键词
# keyword-filter = (null)

[Proxy]
Direct = direct
Reject = reject

[Proxy Group]
Proxy = select, DIRECT, Auto, HK, TW, JP, SG, US, Bitcloud, Pigcloud, Semi

Telegram = select, Proxy, SG

Netflix = select, HK, SG, US, Pigcloud

Emby = select, DIRECT, HK

Bilibili = select, DIRECT, HK, TW

Guard = select, REJECT, DIRECT

Final = select, Proxy, DIRECT

Auto = url-test, policy-path=你的订阅连接, interval=600, tolerance=0, update-interval=86400, hidden=1

HK = url-test, policy-path=你的订阅连接, interval=600, tolerance=0, update-interval=86400, policy-regex-filter=(港|HK|(?i)Hong), hidden=1

TW = url-test, policy-path=你的订阅连接, interval=600, tolerance=0, update-interval=86400, policy-regex-filter=(台湾|台灣|TW|(?i)Taiwan), hidden=1

JP = url-test, policy-path=你的订阅连接, interval=600, tolerance=0, update-interval=86400, policy-regex-filter=(日本|JP|(?i)Japan), hidden=1

SG = url-test, policy-path=你的订阅连接, interval=600, tolerance=0, update-interval=86400, policy-regex-filter=(新加坡|狮城|坡|SG|(?i)Singapore), hidden=1

US = url-test, policy-path=你的订阅连接, interval=600, tolerance=0, update-interval=86400, policy-regex-filter=(美国|美國|US|洛杉矶|西雅图|(?i)States|American), hidden=1

Bitcloud = url-test, policy-path=你的订阅连接, interval=600, tolerance=0, update-interval=86400, hidden=1

Pigcloud = url-test, policy-path=你的订阅连接, interval=600, tolerance=0, update-interval=86400, hidden=1

Semi = url-test, policy-path=你的订阅连接, interval=600, tolerance=0, update-interval=86400, hidden=1

[Rule]
DOMAIN,Amytele.com,Proxy

DOMAIN,nfmovies.com,DIRECT

# 屏蔽YouTube的UDP
AND,((PROTOCOL,UDP),(DOMAIN-SUFFIX,googlevideo.com)),REJECT-NO-DROP

# Client(仅 macOS)
PROCESS-NAME,UUBooster,Direct
# > Download (仅 macOS)
PROCESS-NAME,aria2c,Direct
PROCESS-NAME,fdm,Direct
PROCESS-NAME,Folx,Direct
PROCESS-NAME,NetTransport,Direct
PROCESS-NAME,Thunder,Direct
PROCESS-NAME,Transmission,Direct
PROCESS-NAME,uTorrent,Direct
PROCESS-NAME,WebTorrent,Direct
PROCESS-NAME,WebTorrent Helper,Direct

# 屏蔽 iOS 系统更新（如需屏蔽iOS系统更新请自行注释掉“#"即可生效）
# DOMAIN,mesu.apple.com,Reject
# DOMAIN,gdmf.apple.com,Reject
# DOMAIN,updates-http.cdn-apple.com,Reject
# DOMAIN,xp.apple.com,Reject

# 后续规则修正
RULE-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Unbreak.list,Direct

# Ad去广告
DOMAIN-SET,https://anti-ad.net/surge2.txt,Guard
DOMAIN-SUFFIX,https://anti-ad.net/surge.txt,Guard

# 广告拦截
RULE-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Guard/Advertising.list,Guard
DOMAIN-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Guard/AdvertisingPlus.list,Guard

# 隐私保护
RULE-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Guard/Privacy.list,Guard

# 应用内追踪
DOMAIN-SET,https://raw.githubusercontent.com/mieqq/mieqq/master/In-AppTracker.txt,Guard

# 运营商劫持或恶意网站
RULE-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Guard/Hijacking.list,Guard

# 国际流媒体服务
RULE-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/StreamingMedia/Streaming.list,Proxy

# Netflix
RULE-SET,https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/Surge/Netflix/Netflix.list,Netflix

# Emby
RULE-SET,https://raw.githubusercontent.com/Tartarus2014/For-own-use/master/Ruleset/Emby/Emby.list,Emby

# BiliBili
RULE-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/StreamingMedia/StreamingSE.list,Bilibili

# Telegram
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Telegram.list,Telegram

# 全球加速
RULE-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Global.list,Proxy

# 中国直连
RULE-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/China.list,Direct

# Local Area Network 局域网
RULE-SET,LAN,Direct

# GeoIP China
GEOIP,CN,Direct

FINAL,Final,dns-failed

[Host]
# Firebase Cloud Messaging
mtalk.google.com = 108.177.125.188

# Google Dl
dl.google.com = server:119.29.29.29
dl.l.google.com = server:119.29.29.29

# TP-Link
tplogin.cn = server:syslib
tplinklogin.net = server:syslib
melogin.cn = server:syslib
falogin.cn = server:syslib

# Apple TestFlight
*testflight.apple.com = server:8.8.4.4

# 解锁了「模块」功能的用户可以使用 General.sgmodule 后可移除 [URL Rewrite] 及 [MITM] 的「hostname = www.google.cn,api.abema.io」部分
# 建议使用 General.sgmodule，其他 .sgmodule 按需加入
# 未解锁「模块」功能的用户不要删除以下内容，参照说明(https://github.com/DivineEngine/Profiles/tree/master/Surge)使用快捷指令更新相关内容。

[URL Rewrite]
# Safari全能搜索
# 以下为Safari全能搜索、需要把Safari的搜索引擎设置为：DuckDuckGo

# gm (Google图片)
^https:\/\/duckduckgo.com\/\?q=gm\+([^&]+).+ https://www.google.com/search?&tbm=isch&q=$1 302

# gh (GitHub)
^https:\/\/duckduckgo.com\/\?q=gh\+([^&]+).+ https://github.com/search?q=$1 302

# tf (Google 搜索 TestFlight)
^https:\/\/duckduckgo.com\/\?q=tf(\+|%20)([^&]+).+ https://www.google.com/search?as_q=$2&as_sitesearch=testflight.apple.com 302

# wb (微博)
^https:\/\/duckduckgo.com\/\?q=wb\+([^&]+).+ https://s.weibo.com/weibo/$1 302

# wx (微信)
^https:\/\/duckduckgo.com\/\?q=wx\+([^&]+).+ https://weixin.sogou.com/weixinwap?query=$1 302

# jd (京东)
^https:\/\/duckduckgo.com\/\?q=jd\+([^&]+).+ https://so.m.jd.com/ware/search.action?keyword=$1 302

# tb (淘宝)
^https:\/\/duckduckgo.com\/\?q=tb\+([^&]+).+ https://s.m.taobao.com/h5?q=$1 302

# tm (天猫)
^https:\/\/duckduckgo.com\/\?q=tm\+([^&]+).+ https://s.m.tmall.com/m/search.htm?q=$1 302

# ytb (YouTube)
^https:\/\/duckduckgo.com\/\?q=ytb\+([^&]+).+ https://www.youtube.com/results?search_query=$1 302

# ph (PornHub)
^https:\/\/duckduckgo.com\/\?q=ph\+([^&]+).+ https://cn.pornhub.com/video/search?search=$1 302

# bi (必应)
^https:\/\/duckduckgo.com\/\?q=bi\+([^&]+).+ https://cn.bing.com/search?q=$1 302

# bd (百度)
^https:\/\/duckduckgo.com\/\?q=bd\+([^&]+).+ https://www.baidu.com/s?wd=$1 302

# ddg (DuckDuckGo)
^https:\/\/duckduckgo.com\/\?q=ddg\+([^&]+).+ https://duckduckgo.com/?ia=about&q=$1 302

# 无指令 (Google)
^https:\/\/duckduckgo.com\/\?q=([^&]+).+ https://www.google.com/search?q=$1 302

# 阻止google.com 跳转到google.com.hk
^https?:\/\/(www\.)?g\.cn https://www.google.com/ncr 302
^https?:\/\/(www\.)?google\.cn https://www.google.com/ncr 302

[Header Rewrite]
# 强制跳转百度UA
^https?:\/\/.*\.baidu\.com header-replace User-Agent "Mozilla/5.0 (iPhone; CPU iPhone OS 13_5 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/14.0.3 Mobile/15E148 Safari/16C50 Quark/604.1 T7/10.3 SearchCraft/2.6.3 (Baidu; P1 8.0.0)"

[MITM]
skip-server-cert-verify = true

hostname = api.m.jd.com, *.bilibili.com, trade-acs.m.taobao.com, mp.weixin.qq.com, ms.jr.jd.com, draw.jdfcloud.com, weixin110.qq.com, duckduckgo.com, api.weibo.cn, mapi.weibo.com, *.uve.weibo.com, -*.weibo.com, security.wechat.com, weixin110.qq.com,  *.baidu.com

ca-passphrase = 4E51EDDE
ca-p12 = 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

[Script]
东东超市兑换奖品 = type=cron,cronexp="57-59,0,1 59,0 0 * * *",wake-system=1,timeout=3600,script-path=https://raw.githubusercontent.com/Aaron-lv/sync/jd_scripts/jd_blueCoin.js,script-update-interval=0

东东农场 = type=cron,cronexp=5 6-18/6 * * *,wake-system=1,timeout=3600,script-path=Script/jd_fruit.js

宠汪汪积分兑换奖品 = type=cron,cronexp="54-59,0-3 0,59 7,8,15,16,23,0 * * *",wake-system=1,timeout=3600,script-path=Script/jd_joy_reward.js

腾讯自选股 = type=cron,cronexp="10 0,16 * * *",wake-system=1,timeout=20,script-path=Script/txstock.js

取关所有主播 = type=cron,cronexp=55 6 * * *,wake-system=1,timeout=3600,script-path=Script/jd_unsubscriLive.js

清空购物车 = type=cron,cronexp=55 17 * * *,wake-system=1,timeout=3600,script-path=Script/jd_cleancart.js

取关店铺商品 = type=cron,cronexp=45 23 * * *,wake-system=1,timeout=20,script-path=https://raw.githubusercontent.com/ChuheGit/1/main/Script/jd_scripts/jd_unsubscribe.js,script-update-interval=0

京东资产变动通知 = type=cron,cronexp="15 9,17 * * *",wake-system=1,timeout=3600,script-path=https://raw.githubusercontent.com/Tartarus2014/Script/master/jd_bean_change.js,script-update-interval=0

京东多合一签到 = type=cron,cronexp=5 0 * * *,wake-system=1,timeout=60,script-path=https://raw.githubusercontent.com/NobyDa/Script/master/JD-DailyBonus/JD_DailyBonus.js

# 微博去广告
wb_launch.js = requires-body=1,script-path=https://raw.githubusercontent.com/yichahucha/surge/master/wb_launch.js,type=http-response,pattern=^https?://(sdk|wb)app\.uve\.weibo\.com(/interface/sdk/sdkad.php|/wbapplua/wbpullad.lua)
wb_ad.js = requires-body=1,max-size=-1,script-path=https://raw.githubusercontent.com/yichahucha/surge/master/wb_ad.js,type=http-response,pattern=^https?://m?api\.weibo\.c(n|om)/2/(statuses/(unread|extend|positives/get|(friends|video)(/|_)(mix)?timeline)|stories/(video_stream|home_list)|(groups|fangle)/timeline|profile/statuses|comments/build_comments|photo/recommend_list|service/picfeed|searchall|cardlist|page|!/(photos/pic_recommend_status|live/media_homelist)|video/tiny_stream_video_list|photo/info|remind/unread_count)

微信去广告 = type=http-response,requires-body=1,max-size=-1,pattern=^https?:\/\/mp\.weixin\.qq\.com\/mp\/getappmsgad\?,script-path=https://raw.githubusercontent.com/yjqiang/surge_scripts/main/scripts/wechat/wechat_public_accounts.js

微信公众号去广告 = type=http-request,pattern=^https://mp\.weixin\.qq\.com/mp/getappmsgad,timeout=30,script-path=https://raw.githubusercontent.com/NobyDa/Script/master/QuantumultX/File/Wechat.js

# 港澳台番剧自动切换地区 & 显示豆瓣评分
Bili Region = type=http-response,pattern=^https:\/\/ap(p|i)\.bilibili\.com\/(pgc\/view\/(v\d\/)?app|x(\/v\d)?\/view\/video)\/(season|online)\?access_key,requires-body=1,max-size=0,script-path=https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/Bili_Auto_Regions.js

# 可选, 适用于搜索指定地区的番剧
Bili Search = type=http-request,pattern=^https:\/\/app\.bilibili\.com\/x\/v\d\/search(\/type)?\?.+?%20(%E6%B8%AF|%E5%8F%B0|%E4%B8%AD)&,script-path=https://raw.githubusercontent.com/NobyDa/Script/master/Surge/JS/Bili_Auto_Regions.js

# Netflix检测
nf_check = type=generic,script-path=https://gist.githubusercontent.com/Hyseen/b06e911a41036ebc36acf04ddebe7b9a/raw/nf_check.js,timeout=30,icon=checkmark.seal.fill,icon-color=#34C759

配置重载=script-path=https://raw.githubusercontent.com/TributePaulWalker/Profiles/main/JavaScript/Surge/Profile-Reload.js,type=generic

# 附带重载配置,Surge Pro标题,可显示启动时间,点击刷新为重载配置
SurgePro_ReloadProfile = type=generic,timeout=10,script-path=https://raw.githubusercontent.com/fishingworld/something/main/PanelScripts/surgepro_reloadprofile.js,argument=icon=crown.fill&color=#f6c970

[Panel]
SurgePro_ReloadProfile = script-name=SurgePro_ReloadProfile,update-interval=1

配置重载 = title=配置重载,content=配置重载,style=info,script-name=配置重载,update-interval=-1

nf_check = script-name=nf_check,title=Netflix 解锁检测,update-interval=-1

