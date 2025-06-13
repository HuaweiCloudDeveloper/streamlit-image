# Jaeger部署指南

## ‌一、环境准备

### 系统配置
> -  服务器：鲲鹏服务器
> -  操作系统：Huawei Cloud EulerOS 2.0 64bit
> - CPU: 2vCPUs 或更高
> - RAM: 4GB 或更大
> - Disk: 至少 40GB

## ‌二、下载安装

### 1.安装conda创建python环境
```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-aarch64.sh
bash Miniconda3-latest-Linux-aarch64.sh   
# 创建环境
conda create -n streamlit_env python=3.10
# 若安装后无法识别 conda 命令，手动添加路径：
echo 'export PATH="~/miniconda3/bin:$PATH"' >> ~/.bashrc    
source ~/.bashrc  
```
### 2.激活环境
```bash
conda activate streamlit_env
```
### 安装streamlit
```bash
pip install streamlit==1.40.1
```
### 验证安装‌
```bash
streamlit hello
```
自动打开浏览器访问 http://localhost:8501 