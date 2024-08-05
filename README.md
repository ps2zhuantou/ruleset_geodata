# 一、 geodata 规则集文件说明
## 1. 文件类型
① Clash geodata 规则集文件，包括：geosite.dat、geoip.dat、Country.mmdb 和 geoip.metadb、ASN.mmdb（仅限 [mihomo 内核](https://github.com/MetaCubeX/mihomo)）等  
② [sing-box](https://github.com/SagerNet/sing-box) geodata 规则集文件，包括：geosite.db 和 geoip.db 等
## 2. 数据源
① 每天凌晨 2 点半（北京时间 UTC+8）自动构建，根据 [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat) 和 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) 进行深度定制，可点击查看包含的[域名列表](https://github.com/DustinWin/domain-list-custom/tree/domains)和 [IP 段列表](https://github.com/DustinWin/geoip/tree/ips)  
② `geosite,fakeip-filter,📌 fakeip 过滤` 源采用 [ShellCrash/public/fake_ip_filter.list](https://github.com/juewuy/ShellCrash/blob/dev/public/fake_ip_filter.list)（sing-box 内核专用，可参考《[ShellCrash 使用 sing-box PuerNya 版内核进行 DNS 分流教程-geodata 方案](https://github.com/DustinWin/clash_singbox-tutorials/blob/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/sing-box/%E8%BF%9B%E9%98%B6%E7%AF%87/ShellCrash%20%E4%BD%BF%E7%94%A8%20sing-box%20PuerNya%20%E7%89%88%E5%86%85%E6%A0%B8%E8%BF%9B%E8%A1%8C%20DNS%20%E5%88%86%E6%B5%81%E6%95%99%E7%A8%8B-geodata%20%E6%96%B9%E6%A1%88.md)》）  
③ `geosite,ads,🛑 广告拦截` 源采用 [privacy-protection-tools/anti-AD](https://github.com/privacy-protection-tools/anti-AD)  
④ `geosite,private,🔒 私有网络` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（仅域名）和 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)（仅域名）组合，并添加主流 [Clash dashboard 在线面板](https://github.com/DustinWin/clash_singbox-tools/tree/main/Clash-dashboard)域名（`clash.razord.top`、`clash.metacubex.one`、`yacd.haishan.me`、`yacd.metacubex.one`、`d.metacubex.one`、`metacubex.github.io` 和 `metacubexd.pages.dev`）  
⑤ `geosite,microsoft-cn,🪟 微软服务` 源采用 [v2fly/domain-list-community/microsoft@cn](https://github.com/v2fly/domain-list-community/blob/master/data/microsoft)  
⑥ `geosite,apple-cn,🍎 苹果服务` 源采用 [v2fly/domain-list-community/apple@cn](https://github.com/v2fly/domain-list-community/blob/master/data/apple)  
⑦ `geosite,google-cn,🇬 谷歌服务` 源采用 [v2fly/domain-list-community/google@cn](https://github.com/v2fly/domain-list-community/blob/master/data/google)  
⑧ `geosite,games-cn,🎮 游戏服务` 源采用 [v2fly/domain-list-community/category-games@cn](https://github.com/v2fly/domain-list-community/blob/master/data/category-games)、[blackmatrix7/ios_rule_script/SteamCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/SteamCN) 和 [blackmatrix7/ios_rule_script/GameDownloadCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Game/GameDownloadCN) 组合  
⑨ `geosite,netflix,🎥 奈飞视频` 源采用 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)  
⑩ `geosite,disney,📽️ 迪士尼+` 源采用 [blackmatrix7/ios_rule_script/Disney](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Disney)  
⑪ `geosite,max,🎞️ Max` 源采用 [blackmatrix7/ios_rule_script/HBO](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/HBO)  
⑫ `geosite,primevideo,🎬 Prime Video` 源采用 [blackmatrix7/ios_rule_script/PrimeVideo](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/PrimeVideo)  
⑬ `geosite,appletv,🍎 Apple TV+` 源采用 [blackmatrix7/ios_rule_script/AppleTV](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/AppleTV)  
⑭ `geosite,youtube,📹 油管视频` 源采用 [blackmatrix7/ios_rule_script/YouTube](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/YouTube)  
⑮ `geosite,tiktok,🎵 TikTok` 源采用 [blackmatrix7/ios_rule_script/TikTok](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/TikTok)  
⑯ `geosite,bilibili,📺 哔哩哔哩` 源采用 [blackmatrix7/ios_rule_script/BiliBili](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BiliBili)  
⑰ `geosite,ai,🤖 人工智能` 源采用 [blackmatrix7/ios_rule_script/OpenAI](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/OpenAI)、[blackmatrix7/ios_rule_script/Copilot](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Copilot)、[blackmatrix7/ios_rule_script/Gemini](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Gemini) 和 [blackmatrix7/ios_rule_script/Claude](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Claude) 组合  
⑱ `geosite,networktest,📈 网络测试` 源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 IPv6 测试域名关键字（`keyword`，包括：`ipv6-test`、`test-ipv6`、`ipv6test` 和 `testipv6`）组合  
⑲ `geosite,proxy,🪜 代理域名` 源采用 [v2fly/domain-list-community/geolocation-!cn](https://github.com/v2fly/domain-list-community/blob/master/data/geolocation-!cn)（删除了带有 `@cn` 和 `@ads` 的域名，并新增了 [gfwlist](https://github.com/gfwlist/gfwlist) 和 v2fly/domain-list-community/cn 中带有 `@!cn` 的域名）和 [blackmatrix7/ios_rule_script/Global](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Global) 组合  
⑳ `geosite,cn,🇨🇳 直连域名` 源采用 [v2fly/domain-list-community/cn](https://github.com/v2fly/domain-list-community/blob/master/data/cn)（删除了带有 `@!cn` 和 `@ads` 的域名，并新增了 v2fly/domain-list-community/geolocation-!cn 中带有 `@cn` 的域名）和 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)（仅域名）  
㉑ `geoip,netflix,🎥 奈飞视频` 源采用 [GeoLite2/netflix.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data) 和 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)（仅 IP）组合  
㉒ `geoip,telegram,📲 电报消息` 源采用 [GeoLite2/telegram.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[Telegram IP 段](https://core.telegram.org/resources/cidr.txt) 和 [blackmatrix7/ios_rule_script/Telegram](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Telegram)（仅 IP）组合  
㉓ `geoip,private,🔒 私有网络` 源采用 [GeoLite2/private.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（仅 IP）和 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)（仅 IP）组合  
㉔ `geoip,cn,🇨🇳 直连 IP` 源采用 [GeoLite2/cn.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip)、[blackmatrix7/ios_rule_script/ChinaIPs](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaIPs) 和 [APNIC/CN](https://ftp.apnic.net/stats/apnic/delegated-apnic-latest) 组合
## 3. 文件下载
**规则集文件包含的规则和下载地址对应关系如下表：**
<table>
  <tr>
    <td><b>规则集文件名称</b></td>
    <td align="center"><b>包含规则</b></td>
    <td><b>GitHub 源</b></td>
    <td><b>jsDelivr 源</b></td>
    <td><b>GitHub Proxy 源</b></td>
  </tr>
  <tr>
    <td>geosite-all.dat</td>
    <td><code>ads</code>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>netflix</code>、<code>disney</code>、<code>max</code>、<code>primevideo</code>、<code>appletv</code>、<code>youtube</code>、<code>tiktok</code>、<code>bilibili</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geosite-all.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite-all.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geosite-all.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-all.db</td>
    <td><code>fakeip-filter</code>、<code>ads</code>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>netflix</code>、<code>disney</code>、<code>max</code>、<code>primevideo</code>、<code>appletv</code>、<code>youtube</code>、<code>tiktok</code>、<code>bilibili</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geosite-all.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite-all.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geosite-all.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-all-lite.dat</td>
    <td><del><code>ads</code></del>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>netflix</code>、<code>disney</code>、<code>max</code>、<code>primevideo</code>、<code>appletv</code>、<code>youtube</code>、<code>tiktok</code>、<code>bilibili</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geosite-all-lite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite-all-lite.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geosite-all-lite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-all-lite.db</td>
    <td><code>fakeip-filter</code>、<del><code>ads</code></del>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>netflix</code>、<code>disney</code>、<code>max</code>、<code>primevideo</code>、<code>appletv</code>、<code>youtube</code>、<code>tiktok</code>、<code>bilibili</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geosite-all-lite.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite-all-lite.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geosite-all-lite.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite.dat</td>
    <td><code>ads</code>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geosite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geosite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite.db</td>
    <td><code>fakeip-filter</code>、<code>ads</code>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geosite.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geosite.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-lite.dat</td>
    <td><del><code>ads</code></del>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geosite-lite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite-lite.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geosite-lite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>geosite-lite.db</td>
    <td><code>fakeip-filter</code>、<del><code>ads</code></del>、<code>private</code>、<code>microsoft-cn</code>、<code>apple-cn</code>、<code>google-cn</code>、<code>games-cn</code>、<code>ai</code>、<code>networktest</code>、<code>proxy</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geosite-lite.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite-lite.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geosite-lite.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-all.dat</td>
    <td rowspan="4" align="center"><a href="https://github.com/Loyalsoldier/geoip/tree/release/text">点此查看</a></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip-all.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip-all.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip-all.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-all.mmdb</td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country-all.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country-all.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country-all.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-all.metadb</td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip-all.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip-all.metadb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip-all.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-all.db</td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geoip-all.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geoip-all.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geoip-all.db">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-ASN-all.mmdb</td>
    <td><code>cloudflare</code></del>、<code>cloudfront</code>、<code>facebook</code>、<code>fastly</code>、<code>google</code>、<code>netflix</code>、<code>telegram</code> 和 <code>twitter</code>，具体可<a href="https://github.com/Loyalsoldier/geoip/blob/master/asn.csv">点此查看</a></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country-ASN-all.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country-ASN-all.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country-ASN-all.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.dat</td>
    <td rowspan="4"><code>netflix</code>、<code>telegram</code>、<code>private</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country.mmdb</td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.metadb</td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.metadb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip.db</td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geoip.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geoip.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geoip.db">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.dat</td>
    <td rowspan="4"><del><code>netflix</code></del>、<code>telegram</code>、<code>private</code> 和 <code>cn</code></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip-lite.dat">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip-lite.dat">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip-lite.dat">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-lite.mmdb</td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country-lite.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country-lite.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country-lite.mmdb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.metadb</td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip-lite.metadb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip-lite.metadb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/geoip-lite.metadb">点此下载</a></td>
  </tr>
  <tr>
    <td>geoip-lite.db</td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geoip-lite.db">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geoip-lite.db">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box/geoip-lite.db">点此下载</a></td>
  </tr>
  <tr>
    <td>Country-ASN.mmdb</td>
    <td><code>netflix</code>、<code>telegram</code>、<del><code>private</code> 和 <code>cn</code></del>，具体可<a href="https://github.com/DustinWin/geoip/blob/master/asn.csv">点此查看</a></td>
    <td><a href="https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country-ASN.mmdb">点此下载</a></td>
    <td><a href="https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country-ASN.mmdb">点此下载</a></td>
    <td><a href="https://mirror.ghproxy.com/https://github.com/DustinWin/ruleset_geodata/releases/download/clash/Country-ASN.mmdb">点此下载</a></td>
  </tr>
</table>

## 4. 文件导入
<details>
<summary>① 导入到 Linux 端（以 <a href="https://github.com/juewuy/ShellCrash">ShellCrash</a> 导入 geosite.dat、geosite.db、geoip.dat、Country.mmdb、geoip.metadb、ASN.mmdb 和 geoip.db 为例）</summary>

连接 SSH 后执行如下命令：
```
# 适用于 Clash 内核
curl -o $CRASHDIR/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.dat
curl -o $CRASHDIR/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.dat
curl -o $CRASHDIR/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country.mmdb
# 适用于 mihomo 内核
curl -o $CRASHDIR/geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.metadb
curl -o $CRASHDIR/ASN.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country-ASN.mmdb
# 适用于 sing-box 内核
curl -o $CRASHDIR/geosite.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geosite.db
curl -o $CRASHDIR/geoip.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box/geoip.db
$CRASHDIR/start.sh restart
```
</details>
<details>
<summary>② 导入到 Windows 端（以 <a href="https://github.com/clash-verge-rev/clash-verge-rev">Clash Verge</a> 导入 geosite.dat、geoip.dat、Country.mmdb、geoip.metadb 和 ASN.mmdb 为例）</summary>

以管理员身份运行 CMD 命令提示符，执行如下命令：
```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geosite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.dat
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.dat
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country.mmdb
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.metadb
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\ASN.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country-ASN.mmdb
```
</details>

## 5. 文件拓展
<details>
<summary>① <a href="https://github.com/DustinWin/ruleset_geodata/tree/clash-config">user.yaml</a>（仅限 mihomo 内核）</summary>

注：
- 1. 每天凌晨 3 点（北京时间）自动构建
- 2. 含有“fakeip”字样的 .yaml 配置文件才含有 `fake-ip-filter` 参数的数据

**配置文件名关键字与使用场景对应关系如下表：**
|文件名关键字|使用场景|
|-----|-----|
|lite|无广告拦截，搭配 AdGuardHome|
|noprocess|不含进程匹配模式，仅适合 ShellCrash|

• `fake-ip-filter` 参数  
`fake-ip-filter` 中添加 [ShellCrash/public/fake_ip_filter.list](https://github.com/juewuy/ShellCrash/blob/dev/public/fake_ip_filter.list)（已添加 AdGuardHome 相关域名，包括：`adguardteam.github.io`、`adrules.top`、`anti-ad.net` 和 `static.adtidy.org`，防止作为下游时检查更新和下载“DNS 黑名单”失败），提高兼容性  
`fake-ip-filter` 中添加 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)，防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>

若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/ruleset_geodata/fork)后编辑 *.github/workflows/config.yml* 文件内的 ```name: Generate `clash` geodata-xxx-user.yaml``` 部分  
若 DNS 模式选用的是 `redir-host`，必须进行 DNS 分流（可以参考 [mihomo 内核 DNS 分流教程](https://github.com/DustinWin/clash_singbox-tutorials/tree/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/Clash/%E8%BF%9B%E9%98%B6%E7%AF%87)），可以进入 *.github/workflows/config.yml* 文件，编辑 ```Generate `clash` geodata-redirhost-user.yaml``` 部分  
• 导入 Linux 端（以导入 ShellCrash 为例）  
连接 SSH 后执行如下命令：
- 注：将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）

```
curl -o $CRASHDIR/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/geodata-{DNS 模式}-user-lite-noprocess.yaml
$CRASHDIR/start.sh restart
```
• 导入 Windows 端（以导入 Clash Verge 为例）  
以管理员身份打开 CMD 命令提示符，执行如下命令：
- 注：将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）

```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\profiles\Merge.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/geodata-{DNS 模式}-user.yaml
```
</details>
<details>
<summary>② <a href="https://github.com/DustinWin/ruleset_geodata/tree/sing-box-config">dns.json</a>（仅限 <a href="https://github.com/PuerNya/sing-box/tree/building">sing-box PuerNya 版内核</a>）</summary>

注：
- 1. 每天凌晨 3 点（北京时间）自动构建
- 2. 含有“lite”后缀的 .json 配置文件适合无 sing-box 广告拦截且配合 [AdGuardHome](https://github.com/AdguardTeam/AdGuardHome) 的方案

• `dns.fakeip.exclude_rule` 数组  
`dns.fakeip.exclude_rule` 中的 `"geosite": [ "fakeip-filter" ]` 添加 [ShellCrash/public/fake_ip_filter.list](https://github.com/juewuy/ShellCrash/blob/dev/public/fake_ip_filter.list)（已添加 AdGuardHome 相关域名，包括：`adguardteam.github.io`、`adrules.top`、`anti-ad.net` 和 `static.adtidy.org`，防止作为下游时检查更新和下载“DNS 黑名单”失败），提高兼容性  
`dns.fakeip.exclude_rule` 中的 `"geosite": [ "private" ]` 添加 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)，防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>

若想自己生成配置文件 dns.json，可以 [Fork 本项目](https://github.com/DustinWin/ruleset_geodata/fork)后编辑 *.github/workflows/config.yml* 文件内的 ```Generate `sing-box` geodata-xxx-dns-xxx.json``` 部分  
• 导入 Linux 端（以导入 ShellCrash 为例）   
连接 SSH 后执行如下命令：
- 注：将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `mix`）

```
curl -o $CRASHDIR/jsons/dns.json -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-config/geodata-{DNS 模式}-dns-lite.json
$CRASHDIR/start.sh restart
```
</details>
<details>
<summary>③ 添加定时任务（以 ShellCrash 为例，安装路径为 <i>/data/ShellCrash</i>）</summary>

连接 SSH 后执行 `vi $CRASHDIR/task/task.user`，按一下 Ins 键（Insert 键），粘贴如下内容：
- 注：将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）

```
# 适用于 Clash 内核
201#curl -o /data/ShellCrash/GeoSite.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.dat && curl -o /data/ShellCrash/GeoIP.dat -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.dat && curl -o /data/ShellCrash/Country.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country.mmdb && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新geodata路由规则文件
# 适用于 mihomo 内核
202#curl -o /data/ShellCrash/geoip.metadb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.metadb && curl -o /data/ShellCrash/ASN.mmdb -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/Country-ASN.mmdb && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新geodata路由规则文件
203#curl -o /data/ShellCrash/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/geodata-{DNS 模式}-user-lite-noprocess.yaml && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新user.yaml
# 适用于 sing-box 内核
204#curl -o /data/ShellCrash/geosite.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geosite.db && curl -o /data/ShellCrash/geoip.db -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash/geoip.db && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新geodata路由规则文件
```
按一下 Esc 键（退出键），输入英文冒号 `:`，继续输入 `wq` 并回车  
执行 `crash`，进入 ShellCrash -> 5 配置自动任务 -> 1 添加自动任务，可以看到末尾就有添加的定时任务，输入对应的数字并回车后可设置执行条件
</details>

# 二、 ruleset 规则集文件说明
## 1. 文件类型
① Clash ruleset 规则集文件，格式为 `.yaml`（`format: yaml`）、`.list`（`format: text`） 和 `.mrs`（`format: mrs`）  
② sing-box ruleset 规则集文件，格式有 `.srs`（`"format": "binary"`）和 `.json`（`"format": "source"`）
## 2. 数据源
① 每天凌晨 2 点半（北京时间 UTC+8）自动构建，根据 [Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules) 和 [Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip) 进行深度定制，可点击查看包含的[域名列表](https://github.com/DustinWin/domain-list-custom/tree/domains)和 [IP 段列表](https://github.com/DustinWin/geoip/tree/ips)  
② `rule-set,fakeip-filter,📌 fakeip 过滤` 源采用 [ShellCrash/public/fake_ip_filter.list](https://github.com/juewuy/ShellCrash/blob/dev/public/fake_ip_filter.list)（sing-box 内核专用，可参考《[ShellCrash 使用 sing-box PuerNya 版内核进行 DNS 分流教程-ruleset方案](https://github.com/DustinWin/clash_singbox-tutorials/blob/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/sing-box/%E8%BF%9B%E9%98%B6%E7%AF%87/ShellCrash%20%E4%BD%BF%E7%94%A8%20sing-box%20PuerNya%20%E7%89%88%E5%86%85%E6%A0%B8%E8%BF%9B%E8%A1%8C%20DNS%20%E5%88%86%E6%B5%81%E6%95%99%E7%A8%8B-ruleset%E6%96%B9%E6%A1%88.md)》）  
③ `rule-set,ads,🛑 广告拦截` 源采用 [privacy-protection-tools/anti-AD](https://github.com/privacy-protection-tools/anti-AD)  
④ `rule-set,applications,🖥️ 直连软件` 源采用 [blackmatrix7/ios_rule_script/Download](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Download) 和 [Loyalsoldier/clash-rules/applications.txt](https://github.com/Loyalsoldier/clash-rules/blob/release/applications.txt) 组合  
⑤ `rule-set,private,🔒 私有网络` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（仅域名）和 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)（仅域名）组合，并添加主流 [Clash dashboard 在线面板](https://github.com/DustinWin/clash_singbox-tools/tree/main/Clash-dashboard)域名（`clash.razord.top`、`clash.metacubex.one`、`yacd.haishan.me`、`yacd.metacubex.one`、`d.metacubex.one`、`metacubex.github.io` 和 `metacubexd.pages.dev`）  
⑥ `rule-set,microsoft-cn,🪟 微软服务` 源采用 [v2fly/domain-list-community/microsoft@cn](https://github.com/v2fly/domain-list-community/blob/master/data/microsoft)  
⑦ `rule-set,apple-cn,🍎 苹果服务` 源采用 [v2fly/domain-list-community/apple@cn](https://github.com/v2fly/domain-list-community/blob/master/data/apple)  
⑧ `rule-set,google-cn,🇬 谷歌服务` 源采用 [v2fly/domain-list-community/google@cn](https://github.com/v2fly/domain-list-community/blob/master/data/google)  
⑨ `rule-set,games-cn,🎮 游戏服务` 源采用 [v2fly/domain-list-community/category-games@cn](https://github.com/v2fly/domain-list-community/blob/master/data/category-games)、[blackmatrix7/ios_rule_script/SteamCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/SteamCN) 和 [blackmatrix7/ios_rule_script/GameDownloadCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Game/GameDownloadCN) 组合  
⑩ `rule-set,netflix,🎥 奈飞视频` 源采用 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)（仅域名）  
⑪ `rule-set,disney,📽️ 迪士尼+` 源采用 [blackmatrix7/ios_rule_script/Disney](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Disney)  
⑫ `rule-set,max,🎞️ Max` 源采用 [blackmatrix7/ios_rule_script/HBO](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/HBO)  
⑬ `rule-set,primevideo,🎬 Prime Video` 源采用 [blackmatrix7/ios_rule_script/PrimeVideo](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/PrimeVideo)  
⑭ `rule-set,appletv,🍎 Apple TV+` 源采用 [blackmatrix7/ios_rule_script/AppleTV](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/AppleTV)  
⑮ `rule-set,youtube,📹 油管视频` 源采用 [blackmatrix7/ios_rule_script/YouTube](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/YouTube)  
⑯ `rule-set,tiktok,🎵 TikTok` 源采用 [blackmatrix7/ios_rule_script/TikTok](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/TikTok)  
⑰ `rule-set,bilibili,📺 哔哩哔哩` 源采用 [blackmatrix7/ios_rule_script/BiliBili](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BiliBili)  
⑱ `rule-set,ai,🤖 人工智能` 源采用 [blackmatrix7/ios_rule_script/OpenAI](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/OpenAI)、[blackmatrix7/ios_rule_script/Copilot](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Copilot)、[blackmatrix7/ios_rule_script/Gemini](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Gemini) 和 [blackmatrix7/ios_rule_script/Claude](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Claude) 组合  
⑲ `rule-set,networktest,📈 网络测试` 源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 IPv6 测试域名关键字（`keyword`，包括：`ipv6-test`、`test-ipv6`、`ipv6test` 和 `testipv6`）组合  
⑳ `rule-set,proxy,🪜 代理域名` 源采用 [v2fly/domain-list-community/geolocation-!cn](https://github.com/v2fly/domain-list-community/blob/master/data/geolocation-!cn)（删除了带有 `@cn` 和 `@ads` 的域名，并新增了 [gfwlist](https://github.com/gfwlist/gfwlist) 和 v2fly/domain-list-community/cn 中带有 `@!cn` 的域名）和 [blackmatrix7/ios_rule_script/Global](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Global) 组合  
㉑ `rule-set,cn,🇨🇳 直连域名` 源采用 [v2fly/domain-list-community/cn](https://github.com/v2fly/domain-list-community/blob/master/data/cn)（删除了带有 `@!cn` 和 `@ads` 的域名，并新增了 v2fly/domain-list-community/geolocation-!cn 中带有 `@cn` 的域名）和 [blackmatrix7/ios_rule_script/ChinaMax](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)（仅域名）  
㉒ `rule-set,netflixip,🎥 奈飞视频` 源采用 [GeoLite2/netflix.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)（仅 IP）和 [blackmatrix7/ios_rule_script/Netflix](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)（仅 IP）组合  
㉓ `rule-set,telegramip,📲 电报消息` 源采用 [GeoLite2/telegram.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[Telegram IP 段](https://core.telegram.org/resources/cidr.txt) 和 [blackmatrix7/ios_rule_script/Telegram](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Telegram)（仅 IP）组合  
㉔ `rule-set,privateip,🔒 私有网络` 源采用 [GeoLite2/private.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（仅 IP）和 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)（仅 IP）组合  
㉕ `rule-set,cnip,🇨🇳 直连 IP` 源采用 [GeoLite2/cn.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip)、[blackmatrix7/ios_rule_script/ChinaIPs](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaIPs) 和 [APNIC/CN](https://ftp.apnic.net/stats/apnic/delegated-apnic-latest) 组合
## 3. 文件使用
<details>
<summary>① Clash 内核</summary>

- 注：以下只是节选，请酌情套用

```
proxy-groups:
  - {name: 🚀 节点选择, type: select, proxies: [🇭🇰 香港节点, 🇹🇼 台湾节点, 🇯🇵 日本节点, 🇰🇷 韩国节点, 🇸🇬 新加坡节点, 🇺🇸 美国节点]}
  - {name: 🐟 漏网之鱼, type: select, proxies: [🚀 节点选择, 🎯 全球直连]}
  - {name: 📈 网络测试, type: select, proxies: [🎯 全球直连, 🇭🇰 香港节点, 🇹🇼 台湾节点, 🇯🇵 日本节点, 🇰🇷 韩国节点, 🇸🇬 新加坡节点, 🇺🇸 美国节点]}
  - {name: 🤖 人工智能, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点, 🇺🇸 美国节点]}
  - {name: 🎮 游戏服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🪟 微软服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🇬 谷歌服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🍎 苹果服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🎥 奈飞视频, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 📽️ 迪士尼+, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🎞️ Max, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🎬 Prime Video, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🍎 Apple TV+, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 📹 油管视频, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🎵 TikTok, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 📺 哔哩哔哩, type: select, proxies: [🎯 全球直连, 🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}
  - {name: 🇨🇳 直连域名, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🇨🇳 直连 IP, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}
  - {name: 🪜 代理域名, type: select, proxies: [🚀 节点选择, 🎯 全球直连]}
  - {name: 📲 电报消息, type: select, proxies: [🚀 节点选择]}
  - {name: 🖥️ 直连软件, type: select, proxies: [🎯 全球直连]}
  - {name: 🔒 私有网络, type: select, proxies: [🎯 全球直连]}
  - {name: 🛑 广告拦截, type: select, proxies: [REJECT]}
  - {name: 🎯 全球直连, type: select, proxies: [DIRECT]}

rule-providers:
  ads:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/ads.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/ads.mrs"
    interval: 86400

  applications:
    type: http
    behavior: classical
    format: text
    path: ./rules/applications.list
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/applications.list"
    interval: 86400

  private:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/private.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/private.mrs"
    interval: 86400

  microsoft-cn:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/microsoft-cn.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/microsoft-cn.mrs"
    interval: 86400

  apple-cn:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/apple-cn.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/apple-cn.mrs"
    interval: 86400

  google-cn:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/google-cn.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/google-cn.mrs"
    interval: 86400

  games-cn:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/games-cn.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/games-cn.mrs"
    interval: 86400

  netflix:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/netflix.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/netflix.mrs"
    interval: 86400

  disney:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/disney.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/disney.mrs"
    interval: 86400

  max:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/max.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/max.mrs"
    interval: 86400

  primevideo:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/primevideo.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/primevideo.mrs"
    interval: 86400

  appletv:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/appletv.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/appletv.mrs"
    interval: 86400

  youtube:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/youtube.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/youtube.mrs"
    interval: 86400

  tiktok:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/tiktok.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/tiktok.mrs"
    interval: 86400

  bilibili:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/bilibili.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/bilibili.mrs"
    interval: 86400

  ai:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/ai.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/ai.mrs"
    interval: 86400

  networktest:
    type: http
    behavior: classical
    format: text
    path: ./rules/networktest.list
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/networktest.list"
    interval: 86400

  proxy:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/proxy.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/proxy.mrs"
    interval: 86400

  cn:
    type: http
    behavior: domain
    format: mrs
    path: ./rules/cn.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/cn.mrs"
    interval: 86400

  netflixip:
    type: http
    behavior: ipcidr
    format: mrs
    path: ./rules/netflixip.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/netflixip.mrs"
    interval: 86400

  telegramip:
    type: http
    behavior: ipcidr
    format: mrs
    path: ./rules/telegramip.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/telegramip.mrs"
    interval: 86400

  privateip:
    type: http
    behavior: ipcidr
    format: mrs
    path: ./rules/privateip.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/privateip.mrs"
    interval: 86400

  cnip:
    type: http
    behavior: ipcidr
    format: mrs
    path: ./rules/cnip.mrs
    url: "https://github.com/DustinWin/ruleset_geodata/releases/download/clash-ruleset/cnip.mrs"
    interval: 86400

rules:
  - RULE-SET,ads,🛑 广告拦截
  - RULE-SET,applications,🖥️ 直连软件
  - RULE-SET,private,🔒 私有网络
  - RULE-SET,microsoft-cn,🪟 微软服务
  - RULE-SET,apple-cn,🍎 苹果服务
  - RULE-SET,google-cn,🇬 谷歌服务
  - RULE-SET,games-cn,🎮 游戏服务
  - RULE-SET,netflix,🎥 奈飞视频
  - RULE-SET,disney,📽️ 迪士尼+
  - RULE-SET,max,🎞️ Max
  - RULE-SET,primevideo,🎬 Prime Video
  - RULE-SET,appletv,🍎 Apple TV+
  - RULE-SET,youtube,📹 油管视频
  - RULE-SET,tiktok,🎵 TikTok
  - RULE-SET,bilibili,📺 哔哩哔哩
  - RULE-SET,ai,🤖 人工智能
  - RULE-SET,networktest,📈 网络测试
  - RULE-SET,proxy,🪜 代理域名
  - RULE-SET,cn,🇨🇳 直连域名
  - RULE-SET,netflixip,🎥 奈飞视频,no-resolve
  - RULE-SET,telegramip,📲 电报消息,no-resolve
  - RULE-SET,privateip,🔒 私有网络,no-resolve
  - RULE-SET,cnip,🇨🇳 直连 IP
```
</details>
<details>
<summary>② sing-box 内核</summary>

注：
- 1. 须手动新建“*ruleset*”文件夹，否则规则集文件不会保存在本地。如导入 ShellCrash，可先连接 SSH 后执行命令 `mkdir -p $CRASHDIR/ruleset/`
- 2. 以下只是节选，请酌情套用

```
{
  "outbounds": [
    { "tag": "🚀 节点选择", "type": "selector", "outbounds": [ "🇭🇰 香港节点", "🇹🇼 台湾节点", "🇯🇵 日本节点", "🇰🇷 韩国节点", "🇸🇬 新加坡节点", "🇺🇸 美国节点" ] },
    { "tag": "🐟 漏网之鱼", "type": "selector", "outbounds": [ "🚀 节点选择", "🎯 全球直连" ] },
    { "tag": "📈 网络测试", "type": "selector", "outbounds": [ "🎯 全球直连", "🇭🇰 香港节点", "🇹🇼 台湾节点", "🇯🇵 日本节点", "🇰🇷 韩国节点", "🇸🇬 新加坡节点", "🇺🇸 美国节点" ] },
    { "tag": "🤖 人工智能", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点", "🇺🇸 美国节点" ] },    
    { "tag": "🎮 游戏服务", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🪟 微软服务", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🇬 谷歌服务", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🍎 苹果服务", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🎥 奈飞视频", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "📽️ 迪士尼+", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🎞️ Max", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🎬 Prime Video", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🍎 Apple TV+", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "📹 油管视频", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🎵 TikTok", "type": "selector", "outbounds": [ "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "📺 哔哩哔哩", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择", "🇭🇰 香港节点", "🇯🇵 日本节点", "🇸🇬 新加坡节点" ] },
    { "tag": "🇨🇳 直连域名", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🇨🇳 直连 IP", "type": "selector", "outbounds": [ "🎯 全球直连", "🚀 节点选择" ] },
    { "tag": "🪜 代理域名", "type": "selector", "outbounds": [ "🚀 节点选择", "🎯 全球直连" ] },
    { "tag": "📲 电报消息", "type": "selector", "outbounds": ["🚀 节点选择"] },
    { "tag": "🖥️ 直连软件", "type": "selector", "outbounds": ["🎯 全球直连"] },
    { "tag": "🔒 私有网络", "type": "selector", "outbounds": ["🎯 全球直连"] },
    { "tag": "🛑 广告拦截", "type": "selector", "outbounds": ["REJECT"] },
    { "tag": "🎯 全球直连", "type": "selector", "outbounds": ["DIRECT"] },
    { "tag": "REJECT", "type": "block" },
    { "tag": "DIRECT", "type": "direct" },
    { "tag": "GLOBAL", "type": "selector", "outbounds": [ "DIRECT", "REJECT", "🇭🇰 香港节点", "🇹🇼 台湾节点", "🇯🇵 日本节点", "🇰🇷 韩国节点", "🇸🇬 新加坡节点", "🇺🇸 美国节点" ] },
  ],
  "route": {
    "rules": [
      { "rule_set": [ "ads" ], "outbound": "🛑 广告拦截" },
      { "rule_set": [ "applications" ], "outbound": "🖥️ 直连软件" },
      { "rule_set": [ "private" ], "outbound": "🔒 私有网络" },
      { "rule_set": [ "microsoft-cn" ], "outbound": "🪟 微软服务" },
      { "rule_set": [ "apple-cn" ], "outbound": "🍎 苹果服务" },
      { "rule_set": [ "google-cn" ], "outbound": "🇬 谷歌服务" },
      { "rule_set": [ "games-cn" ], "outbound": "🎮 游戏服务" },
      { "rule_set": [ "netflix" ], "outbound": "🎥 奈飞视频" },
      { "rule_set": [ "disney" ], "outbound": "📽️ 迪士尼+" },
      { "rule_set": [ "max" ], "outbound": "🎞️ Max" },
      { "rule_set": [ "primevideo" ], "outbound": "🎬 Prime Video" },
      { "rule_set": [ "appletv" ], "outbound": "🍎 Apple TV+" },
      { "rule_set": [ "youtube" ], "outbound": "📹 油管视频" },
      { "rule_set": [ "tiktok" ], "outbound": "🎵 TikTok" },
      { "rule_set": [ "bilibili" ], "outbound": "📺 哔哩哔哩" },
      { "rule_set": [ "ai" ], "outbound": "🤖 人工智能" },
      { "rule_set": [ "networktest" ], "outbound": "📈 网络测试" },
      { "rule_set": [ "proxy" ], "outbound": "🪜 代理域名" },
      { "rule_set": [ "cn" ], "outbound": "🇨🇳 直连域名" },
      { "rule_set": [ "netflixip" ], "outbound": "🎥 奈飞视频", "skip_resolve": true },
      { "rule_set": [ "telegramip" ], "outbound": "📲 电报消息", "skip_resolve": true },
      { "rule_set": [ "privateip" ], "outbound": "🔒 私有网络", "skip_resolve": true },
      { "rule_set": [ "cnip" ], "outbound": "🇨🇳 直连 IP" }
    ],
    "rule_set": [
      {
        "tag": "fakeip-filter",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/fakeip-filter.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/fakeip-filter.srs"
      },
      {
        "tag": "ads",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/ads.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/ads.srs"
      },
      {
        "tag": "applications",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/applications.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/applications.srs"
      },
      {
        "tag": "private",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/private.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/private.srs"
      },
      {
        "tag": "microsoft-cn",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/microsoft-cn.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/microsoft-cn.srs"
      },
      {
        "tag": "apple-cn",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/apple-cn.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/apple-cn.srs"
      },
      {
        "tag": "google-cn",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/google-cn.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/google-cn.srs"
      },
      {
        "tag": "games-cn",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/games-cn.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/games-cn.srs"
      },
      {
        "tag": "netflix",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/netflix.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/netflix.srs"
      },
      {
        "tag": "disney",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/disney.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/disney.srs"
      },
      {
        "tag": "max",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/max.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/max.srs"
      },
      {
        "tag": "primevideo",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/primevideo.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/primevideo.srs"
      },
      {
        "tag": "appletv",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/appletv.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/appletv.srs"
      },
      {
        "tag": "youtube",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/youtube.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/youtube.srs"
      },
      {
        "tag": "tiktok",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/tiktok.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/tiktok.srs"
      },
      {
        "tag": "bilibili",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/bilibili.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/bilibili.srs"
      },
      {
        "tag": "ai",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/ai.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/ai.srs"
      },
      {
        "tag": "networktest",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/networktest.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/networktest.srs"
      },
      {
        "tag": "proxy",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/proxy.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/proxy.srs"
      },
      {
        "tag": "cn",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/cn.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/cn.srs"
      },
      {
        "tag": "netflixip",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/netflixip.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/netflixip.srs"
      },
      {
        "tag": "telegramip",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/telegramip.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/telegramip.srs"
      },
      {
        "tag": "privateip",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/privateip.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/privateip.srs"
      },
      {
        "tag": "cnip",
        "type": "remote",
        "format": "binary",
        "path": "./ruleset/cnip.srs",
        "url": "https://github.com/DustinWin/ruleset_geodata/releases/download/sing-box-ruleset/cnip.srs"
      }
    ]
  }
}
```
</details>

## 4. 文件拓展
<details>
<summary>① <a href="https://github.com/DustinWin/ruleset_geodata/tree/clash-config">user.yaml</a>（仅限 mihomo 内核）</summary>

注：
- 1. 每天凌晨 3 点（北京时间）自动构建  
- 2. 含有“fakeip”字样的 .yaml 配置文件才含有 `fake-ip-filter` 参数的数据

**配置文件名关键字与使用场景对应关系如下表：**
|文件名关键字|使用场景|
|-----|-----|
|lite|无广告拦截，搭配 AdGuardHome|
|noprocess|不含进程匹配模式，仅适合 ShellCrash|

• `fake-ip-filter` 参数  
`fake-ip-filter` 中添加 [ShellCrash/public/fake_ip_filter.list](https://github.com/juewuy/ShellCrash/blob/master/public/fake_ip_filter.list)（已添加 AdGuardHome 相关域名，包括：`adguardteam.github.io`、`adrules.top`、`anti-ad.net` 和 `static.adtidy.org`，防止作为下游时检查更新和下载“DNS 黑名单”失败），提高兼容性  
`fake-ip-filter` 中添加 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)，防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>

若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/ruleset_geodata/fork)后编辑 *.github/workflows/config.yml* 文件内的 ```name: Generate `clash` ruleset-xxx-user.yaml``` 部分  
若 DNS 模式选用的是 `redir-host`，必须进行 DNS 分流（可以参考 [mihomo 内核 DNS 分流教程](https://github.com/DustinWin/clash_singbox-tutorials/tree/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/Clash/%E8%BF%9B%E9%98%B6%E7%AF%87)），可以进入 *.github/workflows/config.yml* 文件，编辑 ```Generate `clash` ruleset-redirhost-user.yaml``` 部分  
• 导入 Linux 端（以导入 ShellCrash 为例）  
连接 SSH 后执行如下命令：
- 注：将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）

```
curl -o $CRASHDIR/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/ruleset-{DNS 模式}-user-lite-noprocess.yaml
$CRASHDIR/start.sh restart
```
• 导入 Windows 端（以导入 Clash Verge 为例）   
以管理员身份打开 CMD 命令提示符，执行如下命令：
- 注：将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）

```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im Clash-Verge*
taskkill /f /t /im clash-meta*
curl -o %APPDATA%\io.github.clash-verge-rev.clash-verge-rev\profiles\Merge.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/ruleset-{DNS 模式}-user.yaml
```
</details>
<details>
<summary>② <a href="https://github.com/DustinWin/ruleset_geodata/tree/sing-box-config">dns.json</a>（仅限 sing-box PuerNya 版内核）</summary>

注：
- 1. 每天凌晨 3 点（北京时间）自动构建
- 2. 含有“lite”后缀的 .json 配置文件适合无 sing-box 广告拦截且配合 [AdGuardHome](https://github.com/AdguardTeam/AdGuardHome) 的方案

• `dns.fakeip.exclude_rule` 数组  
`dns.fakeip.exclude_rule` 中的 `"rule_set": [ "fakeip-filter" ]` 添加 [ShellCrash/public/fake_ip_filter.list](https://github.com/juewuy/ShellCrash/blob/dev/public/fake_ip_filter.list)（已添加 AdGuardHome 相关域名，包括：`adguardteam.github.io`、`adrules.top`、`anti-ad.net` 和 `static.adtidy.org`，防止作为下游时检查更新和下载“DNS 黑名单”失败），提高兼容性  
`dns.fakeip.exclude_rule` 中的 `"rule_set": [ "private" ]` 添加 [TrackersList](https://github.com/XIU2/TrackersListCollection/blob/master/all.txt)，防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>

若想自己生成配置文件 dns.json，可以 [Fork 本项目](https://github.com/DustinWin/ruleset_geodata/fork)后编辑 *.github/workflows/config.yml* 文件内的 ```Generate `sing-box` ruleset-xxx-dns-xxx.json``` 部分  
• 导入 Linux 端（以导入 ShellCrash 为例）   
连接 SSH 后执行如下命令：
- 注：将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `mix`）

```
curl -o $CRASHDIR/jsons/dns.json -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@sing-box-config/ruleset-{DNS 模式}-dns-lite.json
$CRASHDIR/start.sh restart
```
</details>
<details>
<summary>③ 添加定时任务（以 ShellCrash 为例，安装路径为 <i>/data/ShellCrash</i>）</summary>

• 连接 SSH 后执行 `vi $CRASHDIR/task/task.user`，按一下 Ins 键（Insert 键），粘贴如下内容：
- 注：将下面命令中的 `{DNS 模式}` 替换为正在使用的 DNS 模式（`fakeip` 或 `redirhost`）

```
# 适用于 mihomo 内核
201#curl -o /data/ShellCrash/yamls/user.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/ruleset_geodata@clash-config/ruleset-{DNS 模式}-user-lite-noprocess.yaml && /data/ShellCrash/start.sh restart >/dev/null 2>&1#更新user.yaml
```
• 按一下 Esc 键（退出键），输入英文冒号 `:`，继续输入 `wq` 并回车  
• 执行 `crash`，进入 ShellCrash -> 5 配置自动任务 -> 1 添加自动任务，可以看到末尾就有添加的定时任务，输入对应的数字并回车后可设置执行条件
</details>
