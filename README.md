# Quantumult X PCDN 屏蔽规则

将 [Pastebin PCDN 域名列表](https://pastebin.com/cyKBv0qK) 转换成 Quantumult X 可识别的远程分流规则。

## 规则订阅地址

| 文件 | 规则数 | 说明 |
| --- | ---: | --- |
| [Bilibili-PCDN-lite.list](rules/Bilibili-PCDN-lite.list) | 3 | 推荐，尽可能只阻断 B 站 PCDN 相关域名 |
| [Bilibili-PCDN-full.list](rules/Bilibili-PCDN-full.list) | 78 | 完整转换版，移除一条重复规则 |

### 精简版（推荐）
```text
https://raw.githubusercontent.com/LxX669/QuantumultX-Rules/main/rules/Bilibili-PCDN-lite.list
```

### 完整版
```text
https://raw.githubusercontent.com/LxX669/QuantumultX-Rules/main/rules/Bilibili-PCDN-full.list
```

## Quantumult X 添加方法

在 **分流 → 规则资源** 中新增远程资源，粘贴上面的 Raw 链接，选择 `REJECT` 策略并保存。

也可在 Quantumult X 配置的 `[filter_remote]` 节添加，例如：

```ini
[filter_remote]
https://raw.githubusercontent.com/LxX669/QuantumultX-Rules/main/rules/Bilibili-PCDN-lite.list, tag=哔哩哔哩 PCDN, force-policy=reject, enabled=true
```

**注意：** 两个文件选一个订阅即可。建议先用精简版，并观察播放是否受到影响。完整版包含一些可能用于正常 CDN、服务访问与数据上报的域名，不能保证全部规则只阻断 PCDN。

## 来源

- 原文：https://pastebin.com/cyKBv0qK
- 转换日期：2026-11-08
