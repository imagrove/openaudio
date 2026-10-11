# Imagrove OpenAudio

> 基于 ESP32 + Wi-Fi 的开源多房间音频系统。用 Sonos 1/5 的价格，做一套不被任何厂商锁定的全屋声音。

**官网** https://openaudio.imagrove.com ｜ **文档** https://openaudio.imagrove.com/docs ｜ **联系** hello@openaudio.imagrove.com

## 能力

- 全屋同步播放
- 分区独立播放
- 无线 5.1 环绕声（规划中）
- 手机音源接入（AirPlay / 蓝牙 / DLNA / Spotify Connect）
- 智能家居集成（Home Assistant / Music Assistant / ESPHome）
- 低成本扩展：单节点 < ¥200

## 架构

```
音源（AirPlay / 蓝牙 / Spotify / 本地文件）
  → 服务端（树莓派 / Armbian 盒子 / x86 小主机：Snapserver 解码 + 打时间戳 + 分发）
  → 多个 ESP32 节点（Wi-Fi 接收 → 同步播放 → 功放 / 音箱）
```

## 仓库结构

| 目录 | 内容 |
|---|---|
| `firmware/` | ESP32 固件（ESP-IDF） |
| `hardware/` | PCB、原理图、BOM |
| `server/` | Snapserver / AirPlay / 蓝牙 配置模板 |

## 相关仓库

- 文档站（public）：https://github.com/imagrove/openaudio-docs
- 官网门户（public）：https://github.com/imagrove/openaudio.imagrove.com

## 现状

早期阶段：已完成 2 节点 Snapcast 同步与手机音源验证；PCB v1 与固件 v1 开发中。详见官网进度表。

## 许可证

- `firmware/`：GPLv3
- `hardware/`：CERN-OHL-S v2
- `server/` 与根级文件：默认 GPLv3

详见 `LICENSE`。Snapcast 是独立开源项目，与本项目无官方关联。
