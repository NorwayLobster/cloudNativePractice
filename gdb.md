<!--
 * @Author: ChengWang(cheng.wang.801@gmail.com)
 * @Date: 2020-12-02 15:22:29
 * @LastEditors: ChengWang
 * @LastEditTime: 2020-12-02 19:32:05
 * @FilePath: /note/gdb.md
-->


# run:
  step into/over: s, 
     没有源代码的函数进不去: 如动态库,只有可执行文件 
     有源代码的函数可以进去如：自定义函数
  step out: finish

# set 
  help set
  set args ... ...: 设置./a.out arg1 arg2 ...
  set var ...=... : 给程序中变量赋值
# x : 查看内存
  help x
  x /ulf  address

# list:
    按空格可以看更多行

# 调试多线程：
  info threads: 查看所有线程
  thread thread_id: 切换线程
  只运行当前线程： set scheduler-locking on
  运行所有     :  set scheduler-locking off
  指定某线程执行某gdb cmd：thread apply thread_id cmd 
  指定全部线程执行某gdb cmd： thread apply all cmd