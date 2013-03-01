1. 查看系统当前使用的kernel 
    
    uname -a
    输出如下：
    
    Linux jason 3.2.0-38-generic-pae #61-Ubuntu SMP Tue Feb 19 12:39:51 UTC 2013 i686 i686 i386 GNU/Linux
    
    可以看到系统当前使用的kernel为3.2.0-38-generic

2. 查看系统安装了哪些kernel
    
    dpkg --get-selections | grep linux
    
    输出如下:
    
    libselinux1					install
    linux-firmware				install
    linux-generic				install
    linux-generic-pae				install
    linux-headers-3.2.0-37			install
    linux-headers-3.2.0-37-generic		install
    linux-headers-3.2.0-37-generic-pae		install
    linux-headers-3.2.0-38			install
    linux-headers-3.2.0-38-generic		install
    linux-headers-3.2.0-38-generic-pae		install
    linux-headers-generic			install
    linux-headers-generic-pae			install
    linux-image-2.6.38-8-generic		deinstall
    linux-image-3.0.0-28-generic		deinstall
    linux-image-3.0.0-28-generic-pae		deinstall
    linux-image-3.2.0-35-generic		deinstall
    linux-image-3.2.0-35-generic-pae		deinstall
    linux-image-3.2.0-36-generic		deinstall
    linux-image-3.2.0-36-generic-pae		deinstall
    linux-image-3.2.0-37-generic		install
    linux-image-3.2.0-37-generic-pae		install
    linux-image-3.2.0-38-generic		install
    linux-image-3.2.0-38-generic-pae		install
    linux-image-generic				install
    linux-image-generic-pae			install
    linux-libc-dev				install
    linux-sound-base				install
    pptp-linux					install
    syslinux					install
    syslinux-common				install
    syslinux-legacy				install
    util-linux					install    

3. 删除不需要的内核 
    
    sudo apt-get remove linux-headers-3.2.0-37
    sudo apt-get remove linux-headers-3.2.0-37-generic
    sudo apt-get remove linux-image-3.2.0-37-generic 
    sudo apt-get remove linux-image-3.2.0-38-generic-pae

4. 重启系统
