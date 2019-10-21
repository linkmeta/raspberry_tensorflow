# PC 安装tensorflow 环境
## 一、安装Anaconda工具
1.下载并安装
官网下载：https://www.anaconda.com/distribution/
选择python3.7 版本
```
输入命令查看版本：
conda --version
```
2.创建虚拟环境
进入Anaconda Prompt，输入命令：
```
conda create -n my_tensorflow python=3.7.3
```
3.创建完毕后激活虚拟环境
```
conda activate tensorflow
```

## 二、使用conda安装特定版本tensorflow
```
pip uninstall tensorflow
conda install --channel https://conda.anaconda.org/anaconda tensorflow=1.13.1
```

## 三、安装其他工具
1.打开Anaconda Navigator
2.选择enviroment->my_tensorflow
3.勾选软件包安装
```
numpy
keras
opencv
```
