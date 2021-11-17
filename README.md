# CS-APP3e-Labs

实验：[Lab Assignments](http://csapp.cs.cmu.edu/3e/labs.html)

课程：[CMU~213](http://www.cs.cmu.edu/~213/index.html)

## 任务
- [X] Data Lab
- [ ] Bomb Lab
- [ ] Attack Lab
- [ ] Buffer Lab(IA32)
- [ ] Architecture Lab
- [ ] Architecture Lab(Y86)
- [ ] Cache Lab
- [ ] Performance Lab
- [ ] Shell Lab
- [ ] Malloc Lab
- [ ] Proxy Lab

## 问题
编译程序时：

    fatal error: bits/libc-header-start.h: No such file or directory
安装 g++-multilib 解决：

    sudo apt-get install g++-multilib


使用 dlc 时若遇到 dlc: Permission denied 可尝试：

    chmod u+x dlc

运行 sudo apt-get update 时若出现

    Err http://archive.canonical.com natty InRelease    
    Err http://security.ubuntu.com oneiric-security InRelease               
    Err http://extras.ubuntu.com natty InRelease                            
    Err http://security.ubuntu.com oneiric-security Release.gpg
      Temporary failure resolving ‘security.ubuntu.com’

可运行：

    echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf > /dev/null

再重新运行

    sudo apt-get update。


若仍遇到问题：

    E: Could not get lock /var/lib/apt/lists/lock - open (11: Resource temporarily unavailable)
    E: Unable to lock directory /var/lib/apt/lists/

可尝试：

    sudo rm /var/lib/apt/lists/lock
    sudo rm /var/cache/apt/archives/lock
    sudo rm /var/lib/dpkg/lock
