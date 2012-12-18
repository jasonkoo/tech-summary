1. 找到缺失文件所依赖的包
    
    dpkg -S(supply) file-path(eg. /usr/include/stdio.h)

2. 安装依赖包
    
    sudo apt-get install package-name

3. 列出某一软件所有安装文件的安装路径
    
    dpkg -L software-name

4. 删除软件或包
    
    sudo apt-get purge package-name/software-name
