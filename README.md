# 使用 Ubuntu 22.04 作为基础镜像
FROM ubuntu:22.04

# 安装 Shellinabox
RUN apt-get update && \
    apt-get install -y shellinabox && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# 设置 root 用户的密码为 'root'
RUN echo 'root:beat' | chpasswd

# 暴露 22 端口
EXPOSE 22

# 启动 Shellinabox
CMD ["/usr/bin/shellinaboxd", "-t", "-s", "/:LOGIN"]


#指令行

更新系统：

//apt update//
安装基础软件包


//apt install sudo curl wget nano screen git//
安装neofetch工具


//sudo apt install neofetch//
清空终端窗口
clear
调用显示系统信息命令
//neofetch//

来源：https://www.youtube.com/watch?v=ajQo99FLYP4
