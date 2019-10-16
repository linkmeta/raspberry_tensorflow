# Raspberry 4B 

# 一、OpenCV 4.1.0 安装
## 1. 安装软件包
```
$sudo pip3 install numpy
$sudo apt-get install build-essential git cmake pkg-config -y
$sudo apt-get install libjpeg8-dev -y
$sudo apt-get install libtiff5-dev -y
$sudo apt-get install libjasper-dev -y
$sudo apt-get install libpng12-dev -y

$sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev -y

$sudo apt-get install libgtk2.0-dev -y
$sudo apt-get install libatlas-base-dev gfortran -y
```
## 2. 下载OpenCV
```
$cd Downloads
$git clone -b 4.1.0 --recursive https://github.com/opencv/opencv.git
$git clone -b 4.1.0 --recursive https://github.com/opencv/opencv_contrib.git
```
## 3. 配置CMake

创建build目录
```
$cd /home/pi/Downloads/opencv
$mkdir build
$cd build
```
配置Cmake，执行以下命令：
```
$cmake -D CMAKE_BUILD_TYPE=RELEASE \
-D CMAKE_INSTALL_PREFIX=/usr/local \
-D INSTALL_C_EXAMPLES=ON \
-D INSTALL_PYTHON_EXAMPLES=ON \
-D OPENCV_EXTRA_MODULES_PATH=/home/pi/Downloads/opencv_contrib/modules \
-D BUILD_EXAMPLES=ON \
-D WITH_LIBV4L=ON \
-D PYTHON3_EXECUTABLE=/usr/bin/python3.7 \
-D PYTHON_INCLUDE_DIR=/usr/include/python3.7 \
-D PYTHON_LIBRARY=/usr/lib/arm-linux-gnueabihf/libpython3.7m.so \
-D PYTHON3_NUMPY_INCLUDE_DIRS=/usr/lib/python3/dist-packages/numpy/core/include \
..
```
## 4. 编译安装
在Cmake生成Makefile之后，便可进行编译安装：
```
$ make -j4
$ sudo make install
$ sudo ldconfig
```



