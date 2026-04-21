
# 🌐 DisinfoNet Dataset

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-green)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Paper](https://img.shields.io/badge/Paper-Coming_Soon-red)
![GitHub stars](https://img.shields.io/github/stars/Shizi123-China/LPD-Dataset?style=social)

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

## 📋 Data Schema

### 🔗 边表 (`edges.csv`)
| 字段 | 类型 | 说明 |
|:---|:---|:---|
| `source_id` | str | 传播起点 |
| `target_id` | str | 传播终点 |


@article{LPD2024,
  title={LPD Dataset: A Benchmark for Social Network Disinformation Detection and Tracing under Limited Perception},
  author={[Author1], [Author2], [Author3], ...},
  journal={[Journal/Conference Name]},
  volume={},
  pages={},
  year={2024},
  publisher={},
  url={https://github.com/YourOrg/LPD-Dataset}
}
