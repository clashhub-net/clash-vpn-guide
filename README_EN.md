# üöÄ Complete Internet Freedom Guide | Learn Clash from Scratch

[![License](https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-blue.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/clashhub-net/clash-vpn-guide.svg?style=flat-square)](https://github.com/clashhub-net/clash-vpn-guide/stargazers)

> üìñ **Beginner-friendly Clash tutorial - Step by step guide**
> 
> From choosing a VPN service to advanced configuration - Master internet freedom

**[‰∏≠ÊñáÊñáÊ°£](docs/zh/README.md)** | **English**

---

## üìã Table of Contents

- [üåü What is Internet Freedom?](#-what-is-internet-freedom)
- [üéØ Why Clash?](#-why-clash)
- [üì¶ Step 1: Choose a VPN Service](#-step-1-choose-a-vpn-service)
- [üíª Step 2: Download Client](#-step-2-download-client)
- [‚öôÔ∏è Step 3: Configure & Use](#Ô∏?step-3-configure--use)
- [üîß Step 4: Advanced Optimization](#-step-4-advanced-optimization)
- [üí° Pro Tips](#-pro-tips)
- [‚ù?FAQ](#-faq)
- [üìö More Resources](#-more-resources)

---

## üåü What is Internet Freedom?

Internet freedom refers to accessing worldwide content without restrictions:

- üé¨ **Streaming**: Netflix, YouTube, Disney+, HBO Max
- üí¨ **Social**: Twitter, Instagram, Facebook, Telegram
- ü§ñ **AI Tools**: ChatGPT, Claude, Midjourney
- üõ† **Dev Tools**: GitHub, Google Search, Stack Overflow
- üìö **Academic**: Google Scholar, Wikipedia (full version)

### Why Do You Need It?

| Use Case | Purpose |
|----------|---------|
| Work & Study | Access Google, GitHub and dev resources |
| Entertainment | Watch Netflix, YouTube videos |
| AI Tools | Use ChatGPT, Claude and AI assistants |
| E-commerce | Manage Shopify, Amazon stores |
| Stay Connected | Keep in touch with friends abroad |

---

## üéØ Why Clash?

### Clash Advantages

| Feature | Description |
|---------|-------------|
| ‚ú?**Rule-based Routing** | Chinese sites direct, foreign sites proxied |
| ‚ú?**Multi-protocol** | Shadowsocks, V2Ray, Trojan compatible |
| ‚ú?**User-friendly** | GUI interface, easy for beginners |
| ‚ú?**Cross-platform** | Windows, macOS, Linux, iOS, Android |
| ‚ú?**Open Source** | Core features are completely free |
| ‚ú?**Customizable** | Custom rules, scripts enhancement |

### Clash vs Other Tools

| Tool | Ease of Use | Features | Rule Routing | Rating |
|------|-------------|----------|--------------|--------|
| **Clash** | ‚≠ê‚≠ê‚≠ê‚≠ê‚≠?| ‚≠ê‚≠ê‚≠ê‚≠ê‚≠?| ‚ú?| üî• Strongly Recommended |
| v2rayN | ‚≠ê‚≠ê‚≠ê‚≠ê | ‚≠ê‚≠ê‚≠ê‚≠ê | ‚ù?| Good for advanced users |
| Shadowsocks | ‚≠ê‚≠ê‚≠?| ‚≠ê‚≠ê‚≠?| ‚ù?| Traditional choice |

---

## üì¶ Step 1: Choose a VPN Service

### What is a VPN Service Provider?

VPN service providers (called "airports" in Chinese) offer proxy nodes. You need to subscribe to access their services.

### How to Choose a Reliable Provider?

#### ‚ú?Key Metrics

| Metric | Description |
|--------|-------------|
| **Node Quality** | Dedicated line > Relay > Direct |
| **Coverage** | More countries/regions = better |
| **Streaming Unlock** | Netflix, Disney+, HBO support |
| **Uptime** | > 99% is ideal |
| **Support** | TG group/ticket system |
| **Price** | Good value, trial available |

#### üèÜ Recommended Providers

| Name | Features | Price Range | Rating |
|------|----------|------------|--------|
| [**ClashVIP**](https://clashvip.net) | Great value, full streaming unlock, new user deals | $2-10/month | ‚≠ê‚≠ê‚≠ê‚≠ê‚≠?|
| [**ClashHub**](https://clashhub.net) | Optimized routing, gaming acceleration, low latency | $3-12/month | ‚≠ê‚≠ê‚≠ê‚≠ê‚≠?|
| [**CFW Official Nodes**](https://clash-for-windows.net) | Official partnership, stable & reliable | $4-15/month | ‚≠ê‚≠ê‚≠ê‚≠ê |

üí° **Tip**: Use the free trial first, subscribe after testing

#### üîç More Comparisons

Visit [VPN Navigator](https://nav.clashvip.net) for:
- Provider price comparisons
- Node line details
- Real user reviews
- Latest deals & promotions

---

## üíª Step 2: Download Client

### Windows Users

#### Recommended: Clash for Windows

**Download**: [https://clash-for-windows.net](https://clash-for-windows.net)

**Installation Steps**:

1. Visit official website to download latest version
2. Double-click `.exe` installer
3. Choose installation path (default recommended)
4. Click "Install" to complete

**First Run**:

```powershell
# If prompted "Windows protected your PC"
# Click "More info" ‚Ü?"Run anyway"
```

### macOS Users

**Download**: [https://clash-for-windows.net](https://clash-for-windows.net)

**Installation Steps**:

1. Download `.dmg` file
2. Double-click to open, drag to Applications
3. Right-click ‚Ü?Open (bypass security check)

**If Blocked**:

```bash
# Run in Terminal (enter password when prompted)
sudo xattr -r -d com.apple.quarantine /Applications/Clash\ for\ Windows.app
```

### iOS Users

#### Recommended: Shadowrocket

**Price**: $3 (one-time purchase)

**Installation**:

1. Search "Shadowrocket" in App Store
2. Purchase and download
3. Copy subscription link ‚Ü?Open App ‚Ü?Auto-detect ‚Ü?Add nodes

#### Free Option: Stash

**Features**: Clash core, rich rules

### Android Users

#### Recommended: Clash for Android

**Download**: [GitHub Release](https://github.com/Kr328/ClashForAndroid/releases)

**Installation**:

1. Download `.apk` file
2. Allow "Install from unknown apps"
3. Open App ‚Ü?Settings ‚Ü?Import subscription

---

## ‚öôÔ∏è Step 3: Configure & Use

### 3.1 Get Subscription Link

1. Log into VPN provider website (e.g. [ClashVIP](https://clashvip.net))
2. Go to "My Subscription" or "User Center"
3. Find and copy "Subscription Link"

> üí° **Note**: Subscription link is private - don't share with others!

### 3.2 Import Subscription

#### Clash for Windows

1. Open software, click "Profiles" on left
2. Paste subscription link in top input
3. Click "Download" to fetch config
4. Click downloaded profile, turns green when active

#### Clash Verge

1. Click "Config" on left
2. Click "New" ‚Ü?select "Remote"
3. Paste subscription link
4. Click the "Use" button on the right of config

### 3.3 Start Proxy

#### System Proxy Mode

| Mode | Description | Use Case |
|------|-------------|----------|
| **System Proxy** | Auto-set IE proxy | Browser access |
| **TUN Mode** | Virtual NIC, full system proxy | Games, CLI tools |

**Recommended Config**:
- Daily use: Enable "System Proxy"
- Gaming: Install "Service Mode" ‚Ü?Enable "TUN Mode"

#### Routing Mode

| Mode | Description |
|------|-------------|
| **Global Mode** | All traffic proxied |
| **Rule Mode** | Auto-route by rules (Recommended) |
| **Direct Mode** | No proxy |

**Recommended**: Choose "Rule Mode" - domestic sites direct, foreign sites proxied

### 3.4 Select Node

1. Click "Proxies" on left
2. Choose appropriate node group (e.g. "Auto", "Proxy")
3. Click the node you want to use

**Node Selection Tips**:

| Use Case | Recommended Node Type |
|----------|----------------------|
| Browsing | Low latency (<200ms) |
| Video Streaming | High bandwidth, streaming unlock |
| Gaming | Dedicated line, latency < 100ms |
| ChatGPT | US node, OpenAI-supported |

---

## üîß Step 4: Advanced Optimization

### 4.1 Custom Rules

#### Rule Types

```yaml
rules:
  - DOMAIN-SUFFIX,google.com,Proxy      # Domain via proxy
  - DOMAIN-SUFFIX,bilibili.com,Direct   # Domain direct
  - DOMAIN-KEYWORD,adserver,REJECT      # Block ads
  - GEOIP,CN,Direct                      # China IP direct
  - MATCH,Proxy                          # Default via proxy
```

#### Adding Custom Rules

1. Open config file (Profiles ‚Ü?click "Edit" on config right side)
2. Add your rules in `rules` section
3. Save and reload config

### 4.2 Enable TUN Mode

**Use Case**: Support games, CLI tools that don't use system proxy

**Steps**:

1. Clash ‚Ü?General ‚Ü?Service Mode ‚Ü?Install
2. Wait for service installation
3. Enable "TUN Mode"

### 4.3 Configure DNS

**Optimize DNS resolution, prevent pollution**:

```yaml
dns:
  enable: true
  enhanced-mode: fake-ip
  nameserver:
    - 223.5.5.5      # Alibaba DNS
    - 119.29.29.29   # Tencent DNS
  fallback:
    - 8.8.8.8        # Google DNS
    - 1.1.1.1        # Cloudflare DNS
  fallback-filter:
    geoip: true
    geoip-code: CN
```

### 4.4 Script Enhancement

**Auto-switch nodes, load balancing and more**:

See [Script Enhancement Guide](docs/en/script-enhancement.md)

---

## üí° Pro Tips

### Keyboard Shortcuts

| Shortcut | Function |
|----------|----------|
| `Ctrl + Shift + C` | Toggle system proxy |
| `Ctrl + Shift + S` | Toggle routing mode |

### Speed Testing

1. **Node Test**: Proxies ‚Ü?click speed test button on node group
2. **Connection Test**: Run in terminal:
   ```bash
   curl -I https://www.google.com
   ```

### Streaming Unlock Detection

Visit these sites to test node streaming support:

- [Netflux](https://netflux.netlify.app/) - Netflix detection
- [Netflix Test Video](https://www.netflix.com/watch/70143404) - Netflix test

---

## ‚ù?FAQ

<details>
<summary><b>Q1: All websites unreachable after enabling proxy?</b></summary>

**A:** Check the following:
1. Is subscription link correctly imported?
2. Is the node working? (click speed test)
3. Is "System Proxy" enabled?
4. Try switching to another node

</details>

<details>
<summary><b>Q2: How to proxy CLI tools?</b></summary>

**A:** Two methods:

**Method 1: Enable TUN Mode** (Recommended)
1. Install Service Mode
2. Enable TUN Mode

**Method 2: Set Environment Variables**
```bash
# Windows PowerShell
$env:HTTP_PROXY = "http://127.0.0.1:7890"
$env:HTTPS_PROXY = "http://127.0.0.1:7890"

# macOS/Linux
export http_proxy=http://127.0.0.1:7890
export https_proxy=http://127.0.0.1:7890
```

</details>

<details>
<summary><b>Q3: Netflix shows "Not Available"?</b></summary>

**A:** Causes:
- Node IP blocked by Netflix
- Node doesn't support that region's content

**Solutions**:
1. Switch to Netflix-supported node (marked "NF")
2. Ask provider support via ticket/TG for recommended nodes
3. Use [Netflix unlock detection](https://netflux.netlify.app/) to test

</details>

<details>
<summary><b>Q4: ChatGPT not working?</b></summary>

**A:** Ensure using OpenAI-supported node:
1. Select US node
2. Avoid Hong Kong, Japan nodes
3. Test at [ChatGPT](https://chat.openai.com)

</details>

<details>
<summary><b>Q5: How to use on mobile?</b></summary>

**A:** 

**iOS (Shadowrocket recommended)**:
1. Purchase Shadowrocket in App Store ($3)
2. Copy subscription link
3. Open App ‚Ü?Auto-detect ‚Ü?Click "Add nodes"

**Android (Clash for Android recommended)**:
1. [Download APK](https://github.com/Kr328/ClashForAndroid/releases)
2. Install ‚Ü?Settings ‚Ü?Import subscription

</details>

---

## üìö More Resources

### Official Resources

- [Clash for Windows Download](https://clash-for-windows.net) - Official client
- [Clash Official Docs](https://lancellc.gitbook.io/clash/) - Detailed config guide

### Recommended Providers

- [ClashVIP](https://clashvip.net) - Great value, new user deals
- [ClashHub](https://clashhub.net) - Optimized routing, gaming
- [VPN Navigator](https://nav.clashvip.net) - Multi-provider comparison

### Community Support

- [ClashHub Community](https://bbs.clashhub.net) - Tutorials, Q&A
- [Telegram Group](https://t.me/clashvpn) - Real-time discussion

### Advanced Learning

- [Custom Rules Tutorial](docs/en/custom-rules.md)
- [Script Enhancement Guide](docs/en/script-enhancement.md)
- [TUN Mode Explained](docs/en/tun-mode.md)

---

## ü§ù Contributing

Found an error or have suggestions? Welcome:

1. Submit [Issue](https://github.com/clashhub-net/clash-vpn-guide/issues)
2. Create [Pull Request](https://github.com/clashhub-net/clash-vpn-guide/pulls)

---

## ‚ö†Ô∏è Disclaimer

This tutorial is for technical exchange and educational purposes only. Please comply with local laws and regulations. Do not use for illegal purposes. Users are responsible for any consequences.

---

## üìú License

[CC BY-NC-SA 4.0](LICENSE) ¬© 2026

---

**üåü If this tutorial helps you, please give a Star!**

---

<p align="center">
  Made with ‚ù§Ô∏è by the community<br>
  <a href="https://clashvip.net">ClashVIP</a> ‚Ä?  <a href="https://clashhub.net">ClashHub</a> ‚Ä?  <a href="https://clash-for-windows.net">CFW Download</a>
</p>
