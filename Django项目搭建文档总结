# Django项目搭建文档（Web）
## python环境安装
Django是一个基于python的开放源代码的Web应用框架，因此第一步，需要在系统中部署python环境，如果用户是linux系统，例如centos7\ubuntu16.04等，系统已经自带python2.7，可以直接使用，如果是windows用户则需要安装，下面以windows10系统为例：

1. 官网下载[python安装包](https://www.python.org/downloads/ ),可以下载压缩包或者安装文件，压缩包下载下来以后解压，安装文件直接安装。
2. 设置windows10系统环境变量，在系统环境变量的path路径下，新增下面两条（前提是你上一步下载的python解压/安装到了对应目录下面）：
```
D:\Program Files\Python27
D:\Program Files\Python27\Scripts
```
3. 打开cmd，输入python，如果进入python环境，证明安装成功

## pip环境安装
pip是python的包管理工具，python项目的开发过程中会引用很多外部包，都需要下载安装，安装了包管理工具可以轻松的通过pip来安装，下面介绍pip安装流程：
1. linux用户下面，以centos7为例，命令行中输入以下三条命令即可快速安装：
```
yum -y install epel-release
yum -y install python-pip
yum clean all
```
2. windows用户采用下面的安装步骤：

    2.1 下载[pip安装包](https://pypi.org/project/pip/#files)

    2.2 cmd下进入解压后的文件夹，找到setup.py文件，在对应目录下执行：
    ```
    python setup.py install
    ```
    2.3 安装成功后，可以 `pip -V` 查看版本。（ps：如果不成功，可以重启一下电脑）
3. 部署好了pip环境后我们可以换一下国内源。因为pip安装python包时候是从远程仓库拉取的，把远程仓库设置成国内源，安装速度会快很多。建议设置。

    3.1 linux用户（centos7下为例）：
    ```
    mkdir -p  ~/.pip/
    touch ~/.pip/pip.conf
    vim ~/.pip/pip.conf  (输入下面国内源)
    ```
    ```
    [global]
    index-url = https://pypi.tuna.tsinghua.edu.cn/simple

    ```
    3.2 windows10用户：
    ```
    在下面路径新建pip.ini文件后输入源信息
    %APPDATA%\pip\pip.ini
    源信息如下：
    [global]
    index-url = https://pypi.tuna.tsinghua.edu.cn/simple
    ``` 

## 安装虚拟环境virtualenv
开发过程中我们可能会根据不同的项目下载很多不同的包，如果不做相应的项目隔离，那么包会越下越多，造成包环境被污染，正确的方式是对不同的项目设置不同的虚拟环境，下载对应的包，让包环境隔离，因此需要virtualenv，
使用下面的命令即可快速安装：
```
pip install virtualenv
virtualenv venv
cd venv
source bin/activate
```
windows下用户使用下面的方式安装：
```
pip install virtualenv
virtualenv venv
cd venv
source Scripts/activate
```
