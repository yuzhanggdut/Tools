# Installing Keras_2.0.4 with CPU for Windows7
## 准备
1. 系统Windows7，64位版本
2. Anaconda3 4.2.0

## 安装步骤
### 1. 由于Keras默认以Tensorflow为backend, 先安装Tensorflow. 打开cmd, 输入以下命令:  
    C:\Users\sweetyu>pip install --upgrade https://storage.googleapis.com/tensorflow/windows/cpu/tensorflow-1.0.1-cp35-cp35m-win_amd64.whl 
### 在安装Tensorflow时, 出现如下错误： 
    Cannot remove entries from nonexistent file d:\python3\lib\site-packages\easy-install.pth
### 解决方法：  
    pip install --ignore-installed setuptools
    再次按照1中安装Tensorflow
### 2. 安装Keras. 同样在cmd中输入以下命令:  
    C:\Users\sweetyu>pip install keras -U --pre  
### 在安装Keras时, 出现了关于scipy的错误: Failed building wheel for scipy. 更新一下scipy即可. 方法如下: 
    a. 前往 http://www.lfd.uci.edu/~gohlke/pythonlibs/#scipy 下载scipy‑0.19.0‑cp35‑cp35m‑win_amd64.whl
    
    b. Pip install scipy‑0.19.0‑cp35‑cp35m‑win_amd64.whl

## 验证安装
### 1. 打开cmd, 输入以下命令:    
    C:\Users\sweetyu>python    
    >>>import keras    
    Using TensorFlow backend.      
如果不报错则安装成功！
### 2. 用Keras中mnist数据集测试个小程序mnist_mlp.py    
    >>> conda install git
    >>> git clone https://github.com/yuzhanggdut/keras.git
    >>> cd keras/examples/mnist_mlp
    >>> python mnist_mlp.py  

## 参考
* [Keras安装和配置指南(Windows)](http://keras-cn.readthedocs.io/en/latest/for_beginners/keras_windows/)  

如有问题欢迎交流！
