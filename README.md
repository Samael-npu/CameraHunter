# Perception Radar -摄像头探测

![Platform](https://img.shields.io/badge/Platform-Android-green.svg) ![Status](https://img.shields.io/badge/Status-Stable-blue.svg) ![License](https://img.shields.io/badge/License-Proprietary-red.svg)

---

## 📖 简介 / Introduction

**Perception Radar** 是一款专为移动端设计的专业级隐私安全审计工具。通过集成多模态传感器数据采集与高精度分析算法，系统能够识别并标定环境中的隐蔽电子设备，如微型摄像头、非法射频监听器及未授权的网络节点。

**Perception Radar** is a professional-grade privacy security audit tool designed for mobile devices. By integrating multi-modal sensor data collection and high-precision analysis algorithms, the system can identify and pinpoint hidden electronic devices, such as pinhole cameras, illicit RF eavesdropping devices, and unauthorized network nodes.

---

## 🛠️ 核心功能 / Core Features

### 1. 多模态融合感知 / Multi-modal Perception
同步分析磁场通量、射频信号（BLE）及声电能量。利用专家加权模型，在复杂背景下输出高置信度的安全警报。
Simultaneously analyzes magnetic flux, RF signals (BLE), and acoustic energy. Uses an expert weighted model to output high-confidence security alerts in complex environments.

### 2. 差分惯性寻向 (罗盘) / Spatial Differential Compass
基于伪合成孔径（Pseudo-SAR）算法，利用陀螺仪与信号强度的相关性，在物理空间中精确标定辐射源的方位。
Based on the Pseudo-SAR algorithm, it uses the correlation between gyroscope data and signal strength to accurately locate radiation sources in physical space.

### 3. 网络节点指纹审计 / Network Fingerprint Audit
集成 TCP 端口探测、RTSP 协议 Banner 抓取及 SSDP 组播嗅探。通过离线 OUI 数据库，识别隐蔽连接的安防终端。
Integrates TCP port probing, RTSP banner grabbing, and SSDP multicast sniffing. Identifies hidden security terminals using an offline OUI database.

### 4. 芯片级热节流分析 / Thermal Throttling Analysis (ICMP)
通过向目标节点注入高频 ICMP 探针，监测响应时间（RTT）的方差变化。利用芯片发热导致的降频特征，识别无被动散热的微型窃密设备。
Analyzes the variance of Round-Trip Time (RTT) by injecting high-frequency ICMP probes. Identifies miniature surveillance devices without passive cooling by detecting frequency scaling signatures caused by chip heat.

### 5. 时域光学过滤 / Time-Domain Optics Analyzer
通过计算环境光差值，滤除背景干扰，仅标定具有高相干反射特征的疑似光学镜头。
By calculating ambient light differentials, it filters background noise to mark only suspected optical lenses with high-coherence reflection signatures.

---

## 📂 使用场景 / Usage Scenarios

| 场景 / Scenario | 审计重点 / Focus | 推荐模式 / Recommended Mode |
| :--- | :--- | :--- |
| **酒店/民宿 (Hotels/Airbnb)** | 隐藏摄像头、路由器镜像节点 | 网络审计 + 光学扫描 (Network + Optics) |
| **更衣室/洗手间 (Fitting Rooms)** | 针孔镜头、本地存储型拍摄设备 | 磁力感知 + 光学模式 (Magnetic + Optics) |
| **商务会议室 (Meeting Rooms)** | 无线窃听器、GSM/BLE 转发器 | 射频审计 + 罗盘定位 (BLE + Spatial) |
| **个人居所 (Private Residence)** | 非授权网络接入、异常声电啸叫 | 全量感知模式 (Full Perception) |

---

## 🚀 技术规格 / Technical Specifications

* **UI Framework**: Jetpack Compose (Declarative UI)
* **Architecture**: MVI (Model-View-Intent)
* **Concurrency**: Kotlin Coroutines & Flow
* **Performance**: JNI C++ Core for Signal Processing
* **Security**: R8 Obfuscation & Algorithm Hardening

---

## 📥 下载与安装 / Download & Installation

本项目仅通过 GitHub Releases 分发已签名的二进制文件（APK）。
This project only distributes signed binary files (APK) via GitHub Releases.

1. 访问 [Releases](../../releases) 页面。
2. 下载最新的 `app-release.apk`。
3. 确保 Android 系统已开启“安装未知应用”权限。

1. Visit the [Releases](../../releases) page.
2. Download the latest `app-release.apk`.
3. Ensure "Install unknown apps" permission is enabled in Android settings.

---

## ⚖️ 法律与版权声明 / Legal & Copyright
* **合规性 (Compliance)**：用户须在合法范围内使用本工具。严禁利用本工具进行任何侵犯他人合法隐私的行为。
* **免责声明 (Disclaimer)**：由于环境干扰及硬件限制，审计结果仅供参考，不构成绝对法律证据。

* **Compliance**: Users must use this tool within legal boundaries. Illicit use for infringing on others' privacy is strictly prohibited.
* **Disclaimer**: Due to environmental interference and hardware limits, audit results are for reference only and do not constitute absolute legal evidence.

---
Copyright © 2026 Perception Radar Team. All rights reserved.
