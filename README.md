
# 🌐 DisinfoNet Dataset

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-green)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
[![Paper](https://img.shields.io/badge/Paper-IEEE-blue)](https://ieeexplore.ieee.org/document/11360386)
![GitHub stars](https://img.shields.io/github/stars/Shizi123-China/DisinfoNet?style=social)

> 📖 **面向受限感知能力条件的社交网络虚假信息检测与溯源基准数据集**  
> 🏛️ 国家重点研发计划“网络空间安全治理”重点专项青年科学家项目 (Grant No. `2022YFB3102600`)
> 
## ⬇️ Data Download

由于数据集原始文件（reprocessed_network.txt）体积过大，无法直接托管在 GitHub 仓库中。请在使用前手动下载并放置到本地目录。

*   **📁 文件名称**: `reprocessed_network.txt` 
*   **☁️ 下载地址**: [Google Drive Link - Click to Download](https://drive.google.com/file/d/159NbiBs0YBKJt_j5oUXkF9uir5sSDBSR/view)
## 📖 Overview

传统社交网络虚假信息研究多基于“全量数据、完整拓扑、充足算力”的理想假设，严重脱离真实业务场景。**DisinfoNet** 数据集首次以**“受限感知”为建模先验**，系统构建了覆盖内容不可得、拓扑不完全、资源受约束、时空不同步等现实约束的标注数据与仿真配置。

本数据集旨在支撑虚假信息**传播动力学建模、监控节点高效优选、多模态快速检测、跨时空精准溯源**等核心任务，为学术界与工业界提供可复现、可对比、可迁移的基准评测平台。

## ✨ Key Features & Highlights

| 受限维度 | 数据集设计特色 | 支撑任务 |
|:---|:---|:---|
| 🕰️ **时空感知受限** | 含跨平台异步传播时间戳、延迟观测模拟序列、局部观测传播轨迹 | 任务1：传播建模 |
| 🌐 **拓扑感知受限** | 提供原始全图 + 多比例剪枝图（10%/30%/50%）+ 隐私脱敏节点ID | 任务4：跨时空溯源 |
| 👁️ **内容感知受限** | 标注内容可获取状态（明文/加密/付费/缺失），提供多模态原始数据与替代特征 | 任务3：多模态检测 |
| ⚙️ **资源感知受限** | 内置不同算力预算下的节点采样配置、模型压缩基准与性能衰减曲线 | 任务2：节点优选 |
| 🎯 **多任务标签** | 同步提供 `检测标签`（图文不符/图像伪造/文本歪曲）、`溯源源集`、`传播风险等级` | 全流程闭环验证 |

## 📁 Dataset Structure
```text
LPD-Dataset/
├── raw/
│   └── a.txt                     # 核心原始传播日志（需从Google Drive下载并放入此目录）
├── processed/                    # (可选) 存放预处理后的数据
├── scripts/                      # 数据加载与评测脚本
│   ├── load_data.py
│   └── evaluation_metrics.py
└── README.md
```

## 📋 Data Schema

### 🔗 边表 (`edges.csv`)
| 字段 | 类型 | 说明 |
|:---|:---|:---|
| `source_id` | str | 传播起点 |
| `target_id` | str | 传播终点 |

## 📚 Citation

If you use this dataset in your research, please cite the following paper:
```text
@INPROCEEDINGS{11360386,
  author={Shi, Jinchen and Yang, Hui and Qiu, Hongjie and Guo, Hao and Luo, Minnan and Zhao, Xiang},
  booktitle={2025 IEEE 10th International Conference on Data Science in Cyberspace (DSC)}, 
  title={DisinfoNet: A Comprehensive Dataset of Disinformation with Contents and Propagation Dynamics Over Social Networks}, 
  year={2025},
  volume={},
  number={},
  pages={303-310},
  keywords={Location awareness;Social networking (online);Noise reduction;Noise;Interference;Internet;Reliability;Information diffusion;Fake news;Faces;Disinformation;Dataset;Network dismantling;Social network},
  doi={10.1109/DSC67331.2025.00046}}
```
---

## ⚖️ License & Ethics

> **🔒 Data License**: This dataset is released under the [**CC BY-NC-SA 4.0**](https://creativecommons.org/licenses/by-nc-sa/4.0/) license. It is strictly for **academic research** purposes only. Commercial use is prohibited.
>
> **⚖️ Compliance Statement**: The dataset has been strictly desensitized in accordance with the *Cybersecurity Law*, *Data Security Law*, and *Personal Information Protection Law* of the PRC. It contains no real privacy information that can identify individuals. Users must sign the "Academic Research Data Usage Commitment" (see `docs/ethics_commitment.pdf`) before use.
>
> **🚫 Prohibited Uses**: Strictly prohibited for training disinformation generation models, coordinating internet water armies, user profiling/tracking, or any other scenarios violating ethics or laws.

---

## 🏛️ 致谢

本数据集由以下单位联合构建：

- 🎓 **国防科技大学** (系统工程学院)
- 🎓 **西安交通大学** (电子与信息学部)
- 🏢 **中国电子科技集团第三十研究所**


---

### ⭐ 支持
如果你觉得  DisinfoNet 有用，请 **Star 本仓库** 并 **引用我们的论文**!
