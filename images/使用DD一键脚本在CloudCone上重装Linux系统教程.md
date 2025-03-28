# 使用DD一键脚本在CloudCone上重装Linux系统教程

## 为什么需要重装系统？
很多用户反馈CloudCone的官方系统镜像不够纯净，使用DD脚本安装时也经常报错。通过本教程，您可以轻松使用一键脚本重新安装纯净的Linux系统。

## 准备工作
在开始前，请确保完成以下准备工作：

1. 更新系统软件包：
   bash
   # Debian/Ubuntu系统：
   apt-get update
   
   # RedHat/CentOS系统：
   yum update
   

2. 安装必要依赖：
   bash
   # Debian/Ubuntu系统：
   apt-get install -y xz-utils openssl gawk file
   
   # RedHat/CentOS系统：
   yum install -y xz openssl gawk file
   

👉 [【点击查看】2025年最新CloudCone优惠码及特价云服务器方案汇总](https://bit.ly/Cloudcone)

## 下载安装脚本
执行以下命令下载DD一键安装脚本：
bash
wget --no-check-certificate -qO InstallNET.sh 'https://moeclub.org/attachment/LinuxShell/InstallNET.sh' && chmod a+x InstallNET.sh

## 系统安装命令大全
根据您需要的系统版本选择对应的安装命令：

### CentOS系统安装
bash
# CentOS 6.10 64位
bash InstallNET.sh -c 6.10 -v 64 -a --mirror 'http://mirror.centos.org/centos'

### Debian系统安装
bash
# Debian 8 64位
bash InstallNET.sh -d 8 -v 64 -a --mirror 'http://mirrors.ustc.edu.cn/debian/'

# Debian 9 64位
bash InstallNET.sh -d 9 -v 64 -a --mirror 'http://mirrors.ustc.edu.cn/debian/'

### Ubuntu系统安装
bash
# Ubuntu 16.10 64位
bash InstallNET.sh -d 16.10 -v 64 -a --mirror 'http://archive.ubuntu.com/ubuntu/'

# Ubuntu 18.10 64位
bash InstallNET.sh -u 18.10 -v 64 -a --mirror 'http://archive.ubuntu.com/ubuntu/'

## 安装后注意事项
1. 安装过程通常需要15-30分钟，请耐心等待
2. 所有系统的root默认密码为：MoeClub.org（安装后请立即修改）
3. 安装完成后，需要通过CloudCone后台的VNC界面进行配置：
   - 进入VNC界面后按键盘的E键
   - 进入Grub配置界面后按Ctrl+C退出
   - 键入exit命令即可正常进入系统

## 常见问题
- 如果遇到安装失败，建议更换镜像源重试
- 部分较新系统版本可能不支持，建议选择稳定版本
- 安装前请确保服务器没有重要数据，此操作会清空所有数据