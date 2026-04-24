
# 🌐 DisinfoNet 数据集

**语言: [English](README-EN.md) | [中文](README-CN.md)**

[![Version](https://img.shields.io/badge/version-1.0.0-blue)](https://github.com/Shizi123-China/DisinfoNet)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-green)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/downloads/release/python-380/)
[![Paper](https://img.shields.io/badge/Paper-IEEE-blue)](https://ieeexplore.ieee.org/document/11360386)
![GitHub stars](https://img.shields.io/github/stars/Shizi123-China/DisinfoNet?style=social)

> 📖 **面向受限感知能力条件的社交网络虚假信息检测与溯源基准数据集**  
> 🏛️ 国家重点研发计划“网络空间安全治理”重点专项青年科学家项目 (Grant No. `2022YFB3102600`)
> 
## ⬇️ 数据下载

由于数据集原始文件（reprocessed_network.txt）体积过大，无法直接托管在 GitHub 仓库中。请在使用前手动下载并放置到本地目录。

*   **📁 文件名称**: `reprocessed_network.txt` 
*   **☁️ 下载地址**: [Google Drive Link - Click to Download](https://drive.google.com/file/d/159NbiBs0YBKJt_j5oUXkF9uir5sSDBSR/view)
## 📖 Overview

传统社交网络虚假信息研究多基于“全量数据、完整拓扑、充足算力”的理想假设，严重脱离真实业务场景。**DisinfoNet** 数据集首次以**“受限感知”为建模先验**，系统构建了覆盖内容不可得、拓扑不完全、资源受约束、时空不同步等现实约束的标注数据与仿真配置。

本数据集旨在支撑虚假信息**传播动力学建模、监控节点高效优选、多模态快速检测、跨时空精准溯源**等核心任务，为学术界与工业界提供可复现、可对比、可迁移的基准评测平台。


## 📁 数据结构
```text
DisinfoNet-Dataset/
├── raw/
│   └── reprocessed_network.txt                     # 核心原始传播日志（需从Google Drive下载并放入此目录）
├── processed/                    # (可选) 存放预处理后的数据
├── scripts/                      # 数据加载与评测脚本
│   ├── load_data.py
│   └── evaluation_metrics.py
└── README.md
```

## 📋 Data Schema

### 🔗 边表 (`reprocessed_network.txt`)
| 字段 | 类型 | 说明 |
|:---|:---|:---|
| `source_id` | str | 传播起点 |
| `target_id` | str | 传播终点 |

## 📚 Citation

如果您在研究中使用本数据集，请引用以下论文：
```text
@INPROCEEDINGS{11360386,
  author={Shi, Jinchen and Yang, Hui and Qiu, Hongjie and Guo, Hao and Luo, Minnan and Zhao, Xiang},
  booktitle={2025 IEEE 10th International Conference on Data Science in Cyberspace (DSC)}, 
  title={DisinfoNet: A Comprehensive Dataset of Disinformation with Contents and Propagation Dynamics Over Social Networks}, 
  year={2025},
  pages={303-310},
  keywords={Location awareness;Social networking (online);Noise reduction;Noise;Interference;Internet;Reliability;Information diffusion;Fake news;Faces;Disinformation;Dataset;Network dismantling;Social network},
  doi={10.1109/DSC67331.2025.00046}}
```
---

## ⚖️ 许可协议与伦理规范

> **🔒 数据许可**: 本数据集基于 [**CC BY-NC-SA 4.0**](https://creativecommons.org/licenses/by-nc-sa/4.0/) 知识共享协议发布。仅限**学术研究**用途，严禁任何商业使用。
>
> **⚖️ 合规声明**: 本数据集已严格按照《中华人民共和国网络安全法》《数据安全法》《个人信息保护法》完成脱敏处理，不含任何可识别自然人的真实隐私信息。
>
> **🚫 禁止用途**: 严禁用于训练虚假信息生成模型、组织网络水军、用户画像追踪，以及其他一切违反伦理道德与法律法规的场景。

---

## 🏛️ 致谢

本数据集由以下单位联合构建：

- 🎓 **国防科技大学** (系统工程学院)
- 🎓 **西安交通大学** (电子与信息学部)
- 🏢 **中国电子科技集团第三十研究所**


---

## ⭐ 支持
如果你觉得  DisinfoNet 有用，请 **Star 本仓库** 并 **引用我们的论文**!
