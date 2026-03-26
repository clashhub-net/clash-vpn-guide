# 自定义规则教程

本教程教你如何自定义 Clash 规则，实现精细化的流量控制。

---

## 📖 规则基础

### 规则类型

| 类型 | 格式 | 示例 |
|------|------|------|
| DOMAIN | 完整域名 | `DOMAIN,google.com,Proxy` |
| DOMAIN-SUFFIX | 域名后缀 | `DOMAIN-SUFFIX,google.com,Proxy` |
| DOMAIN-KEYWORD | 域名关键词 | `DOMAIN-KEYWORD,google,Proxy` |
| IP-CIDR | IP段 | `IP-CIDR,8.8.8.0/24,Proxy` |
| GEOIP | 地理位置 | `GEOIP,CN,Direct` |
| DST-PORT | 目标端口 | `DST-PORT,80,Direct` |

### 策略组

| 策略 | 说明 |
|------|------|
| Proxy | 代理 |
| Direct | 直连 |
| Reject | 拦截 |
| 自定义策略组 | 自己定义的策略组名 |

---

## 🛠 常用规则示例

### 流媒体规则

```yaml
rules:
  # Netflix
  - DOMAIN-SUFFIX,netflix.com,Proxy
  - DOMAIN-SUFFIX,nflxvideo.net,Proxy
  - DOMAIN-SUFFIX,nflxext.com,Proxy
  
  # YouTube
  - DOMAIN-SUFFIX,youtube.com,Proxy
  - DOMAIN-SUFFIX,googlevideo.com,Proxy
  - DOMAIN-SUFFIX,ytimg.com,Proxy
  
  # Disney+
  - DOMAIN-SUFFIX,disneyplus.com,Proxy
  - DOMAIN-SUFFIX,disney-plus.net,Proxy
  
  # HBO Max
  - DOMAIN-SUFFIX,hbomax.com,Proxy
  - DOMAIN-SUFFIX,hbonow.com,Proxy
```

### 开发工具规则

```yaml
rules:
  # GitHub
  - DOMAIN-SUFFIX,github.com,Proxy
  - DOMAIN-SUFFIX,githubusercontent.com,Proxy
  - DOMAIN-SUFFIX,githubassets.com,Proxy
  
  # Google
  - DOMAIN-SUFFIX,google.com,Proxy
  - DOMAIN-SUFFIX,googleapis.com,Proxy
  - DOMAIN-SUFFIX,gstatic.com,Proxy
  
  # Stack Overflow
  - DOMAIN-SUFFIX,stackoverflow.com,Proxy
  - DOMAIN-SUFFIX,stackexchange.com,Proxy
```

### AI服务规则

```yaml
rules:
  # OpenAI
  - DOMAIN-SUFFIX,openai.com,Proxy
  - DOMAIN-SUFFIX,chatgpt.com,Proxy
  - DOMAIN-SUFFIX,ai.com,Proxy
  
  # Anthropic (Claude)
  - DOMAIN-SUFFIX,anthropic.com,Proxy
  - DOMAIN-SUFFIX,claude.ai,Proxy
  
  # Midjourney
  - DOMAIN-SUFFIX,midjourney.com,Proxy
```

### 广告拦截规则

```yaml
rules:
  # 广告域名
  - DOMAIN-KEYWORD,adserver,REJECT
  - DOMAIN-KEYWORD,analytics,REJECT
  - DOMAIN-KEYWORD,tracking,REJECT
  - DOMAIN-SUFFIX,doubleclick.net,REJECT
  - DOMAIN-SUFFIX,googlesyndication.com,REJECT
  
  # 隐私追踪
  - DOMAIN-SUFFIX,google-analytics.com,REJECT
  - DOMAIN-SUFFIX,facebook.com/tr,REJECT
```

### 国内直连规则

```yaml
rules:
  # 常用国内网站
  - DOMAIN-SUFFIX,bilibili.com,DIRECT
  - DOMAIN-SUFFIX,taobao.com,DIRECT
  - DOMAIN-SUFFIX,tmall.com,DIRECT
  - DOMAIN-SUFFIX,jd.com,DIRECT
  - DOMAIN-SUFFIX,qq.com,DIRECT
  - DOMAIN-SUFFIX,weixin.com,DIRECT
  - DOMAIN-SUFFIX,weibo.com,DIRECT
  - DOMAIN-SUFFIX,zhihu.com,DIRECT
  
  # 地理位置分流
  - GEOIP,CN,DIRECT
```

---

## 🎯 进阶技巧

### 策略组配置

```yaml
proxy-groups:
  - name: Proxy
    type: select
    proxies:
      - Auto
      - HongKong
      - Japan
      - US
      - DIRECT
  
  - name: Auto
    type: url-test
    proxies:
      - HK-1
      - HK-2
      - JP-1
      - JP-2
    url: 'http://www.gstatic.com/generate_204'
    interval: 300
  
  - name: Streaming
    type: select
    proxies:
      - Auto
      - US
      - Japan
```

### 规则集引用

使用外部规则集，减少配置文件大小：

```yaml
rule-providers:
  reject:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/Loyalsoldier/clash-rules@release/reject.txt"
    path: ./ruleset/reject.yaml
    interval: 86400

rules:
  - RULE-SET,reject,REJECT
```

---

## 🔗 相关资源

- [Clash官方文档](https://lancellc.gitbook.io/clash/)
- [规则集仓库](https://github.com/Loyalsoldier/clash-rules)
- [广告拦截规则](https://github.com/ACL4SSR/ACL4SSR)

---

**最后更新**：2026-03-26
