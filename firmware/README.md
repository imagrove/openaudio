# firmware

ESP32 固件（基于 ESP-IDF）。

## 计划

- Snapclient 移植（多房间同步、网络音量/静音）
- I2S 输出（48kHz / 16bit 立体声），支持 PCM5102 / TAS5805M 等 DAC / 功放
- Wi-Fi 配网（网页配网 + 预置 Snapserver 地址）
- OTA 更新（签名 + 回滚）
- 默认关闭 Wi-Fi 省电模式，加大音频缓冲以抵抗抖动

## 许可

GPLv3（见仓库根 `LICENSE`）。分发硬件时须提供完整对应源代码。
