# TUN Mode Explained

## What is TUN Mode?

TUN mode creates a virtual network interface to achieve system-wide proxy, supporting all apps (including games, CLI tools) through the proxy.

---

## Why Need TUN Mode?

| Scenario | System Proxy | TUN Mode |
|----------|-------------|----------|
| Browser Access | ✅ Supported | ✅ Supported |
| CLI Tools | ❌ Not supported | ✅ Supported |
| Gaming | ❌ Not supported | ✅ Supported |
| Some Apps | ❌ May not support | ✅ Fully supported |

---

## How to Enable TUN Mode?

### Windows

1. **Install Service Mode**
   - Clash for Windows → General
   - Click "Install" under "Service Mode"
   - Wait for installation to complete

2. **Enable TUN Mode**
   - Toggle "TUN Mode" switch
   - First time will prompt for network permission, click "Allow"

### macOS

1. Clash for Windows → General
2. Enable "TUN Mode"
3. Enter password to authorize

---

## TUN Mode Configuration

```yaml
tun:
  enable: true
  stack: system  # or gvisor
  dns-hijack:
    - any:53
  auto-route: true
  auto-detect-interface: true
```

### stack Parameter

| Parameter | Description | Recommendation |
|-----------|-------------|-----------------|
| system | Use system network stack | Windows recommended |
| gvisor | Userspace network stack | Linux recommended |

---

## Troubleshooting

### Issue 1: Can't Access Internet After Enabling TUN

**Solution**:
1. Check if Service Mode installed successfully
2. Restart Clash
3. Run as administrator

### Issue 2: High Gaming Latency

**Solution**:
1. Select dedicated line nodes
2. Reduce latency with `stack` parameter (use `system`)
3. Check local network

---

**Last Updated**: 2026-03-26
