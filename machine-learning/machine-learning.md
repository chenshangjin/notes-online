[TOC]

# 机器学习环境搭建（conda+CUDA+pytorch）[参考](https://blog.csdn.net/weixin_43282101/article/details/141968743)

## 1.硬件设备与操作系统

|          |                           |
| -------- | ------------------------- |
| 操作系统 | Windows10 64位            |
| CPU      | Intel(R) Core(TM) i9-9900 |
| 内存     | 16G                       |
| GPU      | NVIDIA Quadro P2200       |

## 2.环境搭建

### Python

#### **0.添加阿里云镜像源**

`pip config --global set  global.index-url https://mirrors.aliyun.com/pypi/simple/`

或者临时指定镜像源：`pip install -i https://pypi.tuna.tsinghua.edu.cn/simple  <somepacket>`

其他镜像源：

清华 `https://pypi.tuna.tsinghua.edu.cn/simple`

中国科技大学 `https://pypi.mirrors.ustc.edu.cn/simple/`

默认镜像源 `https://pypi.org/simple`

### Anaconda

Conda是一种流行的Python包管理工具，它可以用于管理Python环境和包。

#### **0.添加清华大学镜像源**

`conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/`

`conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/`

`conda config --set show_channel_urls yes`

#### **1.创建环境**

`conda create -n testProject python=3.8`

#### **2.激活环境**

`conda activate testProject`

#### **3.退出环境**

`conda deactivate`

#### **4.查看已安装的包**

`conda list`

### CUDA

CUDA（Compute Unified Device Architecture）是一种由NVIDIA开发的并行计算平台和编程模型，用于在NVIDIA GPU上运行计算任务。CUDA允许开发者使用C++语言编写程序，并利用GPU的并行处理能力来加速计算任务。

### pytorch

PyTorch是一种开源的机器学习框架，主要用于深度学习。它由Facebook的AI研究实验室（FAIR）开发，并于2017年开源。PyTorch的设计目标是提供一个动态计算图（Dynamic Computation Graph）和自动微分（Automatic Differentiation）的框架，用于快速开发和训练深度学习模型。

`conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia` 





