# TUN 模式详解

## 什么是 TUN 模式？

TUN 模式通过创建虚拟网卡，实现系统级别的全局代理，支持所有应用（包括游戏、命令行工具）走代理。

---

## 为什么需要 TUN 模式？

| 场景 | 系统代理 | TUN模式 |
|------|----------|---------|
| 浏览器访问 | ✅ 支持 | ✅ 支持 |
| 命令行工具 | ❌ 不支持 | ✅ 支持 |
| 游戏加速 | ❌ 不支持 | ✅ 支持 |
| 部分应用 | ❌ 可能不支持 | ✅ 全面支持 |

---

## 如何开启 TUN 模式？

### Windows

1. **安装服务模式**
   - Clash for Windows → General
   - 点击 "Service Mode" 下的 "Install"
   - 等待安装完成

2. **开启 TUN 模式**
   - 点击 "TUN Mode" 开关
   - 首次会弹出网络权限请求，点击"允许"

### macOS

1. Clash for Windows → General
2. 开启 "TUN Mode"
3. 输入密码授权

---

## TUN 模式配置

```yaml
tun:
  enable: true
  stack: system  # 或 gvisor
  dns-hijack:
    - any:53
  auto-route: true
  auto-detect-interface: true
```

### stack 参数说明

| 参数 | 说明 | 推荐 |
|------|------|------|
| system | 使用系统网络栈 | Windows 推荐 |
| gvisor | 用户态网络栈 | Linux 推荐 |

---

## 故障排除

### 问题1：开启 TUN 后无法上网

**解决方案**：
1. 检查 Service Mode 是否安装成功
2. 重启 Clash
3. 以管理员身份运行

### 问题2：游戏延迟高

**解决方案**：
1. 选择专线节点
2. 降低 `stack` 参数的延迟（使用 `system`）
3. 检查本地网络

---

**最后更新**：2026-03-26
