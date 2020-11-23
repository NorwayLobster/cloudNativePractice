<!--
 * @Author: your name
 * @Date: 2020-11-24 00:42:35
 * @LastEditTime: 2020-11-24 00:47:30
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /note/vmware tools.md
-->

https://linuxconfig.org/install-vmware-tools-on-ubuntu-20-04-focal-fossa-linux
# UBUNTU 20.04 SERVER:
$ apt install open-vm-tools
# UBUNTU 20.04 DESKTOP:
$ apt install open-vm-tools-desktop open-vm-tools
reboot

 dpkg -l|grep open-vm
 lsmod | grep vmw

