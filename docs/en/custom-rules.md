# Custom Rules Tutorial

This tutorial teaches you how to customize Clash rules for fine-grained traffic control.

---

## 📖 Rule Basics

### Rule Types

| Type | Format | Example |
|------|--------|---------|
| DOMAIN | Full domain | `DOMAIN,google.com,Proxy` |
| DOMAIN-SUFFIX | Domain suffix | `DOMAIN-SUFFIX,google.com,Proxy` |
| DOMAIN-KEYWORD | Domain keyword | `DOMAIN-KEYWORD,google,Proxy` |
| IP-CIDR | IP range | `IP-CIDR,8.8.8.0/24,Proxy` |
| GEOIP | Geo location | `GEOIP,CN,Direct` |
| DST-PORT | Target port | `DST-PORT,80,Direct` |

### Policy Groups

| Policy | Description |
|--------|-------------|
| Proxy | Use proxy |
| Direct | Direct connection |
| Reject | Block connection |
| Custom groups | Your defined group names |

---

## 🛠 Common Rule Examples

### Streaming Rules

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

### Dev Tools Rules

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

### AI Services Rules

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

### Ad Blocking Rules

```yaml
rules:
  # Ad domains
  - DOMAIN-KEYWORD,adserver,REJECT
  - DOMAIN-KEYWORD,analytics,REJECT
  - DOMAIN-KEYWORD,tracking,REJECT
  - DOMAIN-SUFFIX,doubleclick.net,REJECT
  - DOMAIN-SUFFIX,googlesyndication.com,REJECT
  
  # Privacy trackers
  - DOMAIN-SUFFIX,google-analytics.com,REJECT
  - DOMAIN-SUFFIX,facebook.com/tr,REJECT
```

### China Direct Rules

```yaml
rules:
  # Common Chinese sites
  - DOMAIN-SUFFIX,bilibili.com,DIRECT
  - DOMAIN-SUFFIX,taobao.com,DIRECT
  - DOMAIN-SUFFIX,tmall.com,DIRECT
  - DOMAIN-SUFFIX,jd.com,DIRECT
  - DOMAIN-SUFFIX,qq.com,DIRECT
  - DOMAIN-SUFFIX,weixin.com,DIRECT
  - DOMAIN-SUFFIX,weibo.com,DIRECT
  - DOMAIN-SUFFIX,zhihu.com,DIRECT
  
  # Geo-based routing
  - GEOIP,CN,DIRECT
```

---

## 🎯 Advanced Techniques

### Policy Group Configuration

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

### Rule Provider Reference

Use external rule providers to reduce config file size:

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

## 🔗 Related Resources

- [Clash Official Docs](https://lancellc.gitbook.io/clash/)
- [Rule Sets Repository](https://github.com/Loyalsoldier/clash-rules)
- [Ad Blocking Rules](https://github.com/ACL4SSR/ACL4SSR)

---

**Last Updated**: 2026-03-26
