
# 🌐 DisinfoNet Dataset

[![Version](https://img.shields.io/badge/version-1.0.0-blue)](https://github.com/Shizi123-China/DisinfoNet)
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/license-CC--BY--NC--SA--4.0-green)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/downloads/release/python-380/)
[![Paper](https://img.shields.io/badge/Paper-IEEE-blue)](https://ieeexplore.ieee.org/document/11360386)
![GitHub stars](https://img.shields.io/github/stars/Shizi123-China/DisinfoNet?style=social)

> 📖 **Benchmark Dataset for Social Network Disinformation Detection and Tracing Under Limited Perception Capabilities**  
> 🏛️ Supported by the Young Scientist Project of the National Key R&D Program "Cyberspace Security Governance" Special Project (Grant No. `2022YFB3102600`)
> 
## ⬇️ Data Download

Due to the large file size of the original dataset file (reprocessed_network.txt), it cannot be directly hosted in the GitHub repository. Please manually download it and place it in your local directory before use.

*   **📁 File Name**: `reprocessed_network.txt` 
*   **☁️ Download Link**: [Google Drive Link - Click to Download](https://drive.google.com/file/d/159NbiBs0YBKJt_j5oUXkF9uir5sSDBSR/view)
## 📖 Overview

Traditional research on social network disinformation is mostly based on ideal assumptions of full-scale data, complete topology, and sufficient computing resources, which are severely disconnected from real-world application scenarios. For the first time, the **DisinfoNet** dataset takes limited perception as a modeling prior, and systematically constructs annotated data and simulation configurations covering realistic constraints such as unavailable content, incomplete topology, resource limitations, and spatiotemporal asynchronization.


This dataset supports core tasks including disinformation **propagation dynamics modeling, efficient monitoring node selection, multi-modal rapid detection, and cross-spatiotemporal accurate tracing.** It provides a reproducible, comparable, and transferable benchmark evaluation platform for both academia and industry.


## 📁 Dataset Structure
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

### 🔗 Edge Table (`edges.csv`)
| Field | Type | Description |
|:---|:---|:---|
| `source_id` | str | Propagation source node ID |
| `target_id` | str | 	Propagation destination node ID |

## 📚 Citation

If you use this dataset in your research, please cite the following paper:
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

## ⚖️ License & Ethics

> **🔒 Data License**: This dataset is released under the [**CC BY-NC-SA 4.0**](https://creativecommons.org/licenses/by-nc-sa/4.0/) license. It is strictly for **academic research** purposes only. Commercial use is prohibited.
>
> **⚖️ Compliance Statement**: The dataset has been strictly desensitized in accordance with the *Cybersecurity Law*, *Data Security Law*, and *Personal Information Protection Law* of the PRC. It contains no real privacy information that can identify individuals.
>
> **🚫 Prohibited Uses**: Strictly prohibited for training disinformation generation models, coordinating internet water armies, user profiling/tracking, or any other scenarios violating ethics or laws.

---

## 🏛️ Acknowledgements

This dataset is jointly constructed by the following institutions:

- 🎓 **National University of Defense Technology** (College of Systems Engineering)
- 🎓 **Xi'an Jiaotong University** (Faculty of Electronic and Information Engineering)
- 🏢 **The 30th Research Institute of China Electronics Technology Group Corporation**


---

## ⭐ Support
If you find DisinfoNet helpful, please **star this repository** and **cite our paper!**
