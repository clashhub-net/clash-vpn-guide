# 鑷畾涔夎鍒欐暀绋?
鏈暀绋嬫暀浣犲浣曡嚜瀹氫箟 Clash 瑙勫垯锛屽疄鐜扮簿缁嗗寲鐨勬祦閲忔帶鍒躲€?
---

## 馃摉 瑙勫垯鍩虹

### 瑙勫垯绫诲瀷

| 绫诲瀷 | 鏍煎紡 | 绀轰緥 |
|------|------|------|
| DOMAIN | 瀹屾暣鍩熷悕 | `DOMAIN,google.com,Proxy` |
| DOMAIN-SUFFIX | 鍩熷悕鍚庣紑 | `DOMAIN-SUFFIX,google.com,Proxy` |
| DOMAIN-KEYWORD | 鍩熷悕鍏抽敭璇?| `DOMAIN-KEYWORD,google,Proxy` |
| IP-CIDR | IP娈?| `IP-CIDR,8.8.8.0/24,Proxy` |
| GEOIP | 鍦扮悊浣嶇疆 | `GEOIP,CN,Direct` |
| DST-PORT | 鐩爣绔彛 | `DST-PORT,80,Direct` |

### 绛栫暐缁?
| 绛栫暐 | 璇存槑 |
|------|------|
| Proxy | 浠ｇ悊 |
| Direct | 鐩磋繛 |
| Reject | 鎷︽埅 |
| 鑷畾涔夌瓥鐣ョ粍 | 鑷繁瀹氫箟鐨勭瓥鐣ョ粍鍚?|

---

## 馃洜 甯哥敤瑙勫垯绀轰緥

### 娴佸獟浣撹鍒?
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

### 寮€鍙戝伐鍏疯鍒?
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

### AI鏈嶅姟瑙勫垯

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

### 骞垮憡鎷︽埅瑙勫垯

```yaml
rules:
  # 骞垮憡鍩熷悕
  - DOMAIN-KEYWORD,adserver,REJECT
  - DOMAIN-KEYWORD,analytics,REJECT
  - DOMAIN-KEYWORD,tracking,REJECT
  - DOMAIN-SUFFIX,doubleclick.net,REJECT
  - DOMAIN-SUFFIX,googlesyndication.com,REJECT
  
  # 闅愮杩借釜
  - DOMAIN-SUFFIX,google-analytics.com,REJECT
  - DOMAIN-SUFFIX,facebook.com/tr,REJECT
```

### 鍥藉唴鐩磋繛瑙勫垯

```yaml
rules:
  # 甯哥敤鍥藉唴缃戠珯
  - DOMAIN-SUFFIX,bilibili.com,DIRECT
  - DOMAIN-SUFFIX,taobao.com,DIRECT
  - DOMAIN-SUFFIX,tmall.com,DIRECT
  - DOMAIN-SUFFIX,jd.com,DIRECT
  - DOMAIN-SUFFIX,qq.com,DIRECT
  - DOMAIN-SUFFIX,weixin.com,DIRECT
  - DOMAIN-SUFFIX,weibo.com,DIRECT
  - DOMAIN-SUFFIX,zhihu.com,DIRECT
  
  # 鍦扮悊浣嶇疆鍒嗘祦
  - GEOIP,CN,DIRECT
```

---

## 馃幆 杩涢樁鎶€宸?
### 绛栫暐缁勯厤缃?
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

### 瑙勫垯闆嗗紩鐢?
浣跨敤澶栭儴瑙勫垯闆嗭紝鍑忓皯閰嶇疆鏂囦欢澶у皬锛?
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

## 馃敆 鐩稿叧璧勬簮

- [Clash瀹樻柟鏂囨。](https://lancellc.gitbook.io/clash/)
- [瑙勫垯闆嗕粨搴揮(https://github.com/Loyalsoldier/clash-rules)
- [骞垮憡鎷︽埅瑙勫垯](https://github.com/ACL4SSR/ACL4SSR)

---

**鏈€鍚庢洿鏂?*锛?026-03-26
