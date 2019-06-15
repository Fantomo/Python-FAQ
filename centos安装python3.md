## CentOS 安装python3
#### 下载官网python3 安装包
* wget https://www.python.org/ftp/python/3.7.1/Python-3.7.1.tgz
* 解压 tar -zxvf Python-3.7.1.tgz

#### 安装步骤
* 安装python3.7 需要下载此依赖,否则 异常提示:ModuleNotFoundError: No module named ‘_ctypes’
    > yum install libffi-devel -y 
* 安装依赖
	> yum install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gcc make -y
* 将安装包移动到/usr/local下
	> mv Python-3.7.1 /usr/local
* 在 /usr/local 下创建python3 目录
	> mkdir /usr/local/python3
* 转到解压文件夹下
 	> cd /usr/local/Python-3.7.1
* 配置安装目录
	> ./configure --prefix=/usr/local/python3
* 编译安装源码
	> make && make install
* 设置python3 软链接
	> ln -s /usr/local/python3/bin/python3 /usr/bin/python3
* 设置pip3 软链接
	> ln -s /usr/local/python3/bin/pip3 /usr/bin/pip3	
