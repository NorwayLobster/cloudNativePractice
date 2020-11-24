<!--
 * @Author: your name
 * @Date: 2020-11-22 23:13:53
 * @LastEditTime: 2020-11-22 23:15:04
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /note/ubuntu20-04.md
-->
#  /usr/bin/ld: final link failed: No space left on device
  still not be sloved
#  network problem: can not ping www.qq.com 
	1. restart eth0, etc
	2. reboot vm
	3. reboot host machine
	4. deselect the NAT, and choose NAT again.
# list version of ubuntu 
    lsb_release -a
# check arch 
  dpkg --print-architecture
  dpkg --print-foreign-architectures
  deb [arch=amd64,i386] http://archive.ubuntu.com/ubuntu xenial universe main restricted multiverse

