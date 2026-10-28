# EEG-Acquisition-Device（V1）

基于 **ADS1299 + ESP32-S3** 的 16 通道脑电（EEG）采集硬件工程，使用 Altium Designer 设计。本仓库当前收录 `ADS1299-ESP32-V3` 版本。

## 功能简介

- **脑电采集前端**：两片 ADS1299 构成 16 通道采集硬件，提供 24 位模数转换、输入 RC 滤波、参考电极与偏置电路。
- **主控与接口**：采用 ESP32-S3-WROOM-1-N8，提供 ADS1299 的 SPI 通信及采集控制连接。
- **下载与调试**：提供 USB Type-C、CH340C USB 转串口、自动下载电路以及 BOOT / EN 按键。
- **电源管理**：包含 BQ24075 锂电池充电管理、BQ27441 电量计，以及升降压、负电压生成和线性稳压电路。

上述内容描述硬件设计功能；本次上传不包含 ESP32 固件或上位机程序，实际采样率、增益和数据传输方式由配套固件配置。

## 工程文件

| 文件 | 说明 |
| --- | --- |
| [ADS1299-ESP32-V3.PrjPcb](ADS1299-ESP32-V3/ADS1299-ESP32-V3.PrjPcb) | Altium Designer 工程入口 |
| [ADD1299-V3.SchDoc](ADS1299-ESP32-V3/ADD1299-V3.SchDoc) | ADS1299 采集前端原理图 |
| [ESP32.SchDoc](ADS1299-ESP32-V3/ESP32.SchDoc) | 主控、下载与调试电路原理图 |
| [POWER.SchDoc](ADS1299-ESP32-V3/POWER.SchDoc) | 电源与电池管理原理图 |
| [ADS1299-V3.PcbDoc](ADS1299-ESP32-V3/ADS1299-V3.PcbDoc) | PCB 布局布线文件 |
| [ADS1299-ESP32-V3.pdf](ADS1299-ESP32-V3/ADS1299-ESP32-V3.pdf) | 原理图及 PCB 的 PDF 导出，可直接查看 |
| `ADS1299-ESP32-V3.OutJob` | 输出任务配置 |
| `Project Outputs for ADS1299-ESP32-V3/` 及同名 ZIP | 原工程现有的 Gerber、钻孔、贴片坐标及报告文件 |
