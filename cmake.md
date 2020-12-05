<!--
 * @Author: ChengWang(cheng.wang.801@gmail.com)
 * @Date: 2020-12-02 13:50:22
 * @LastEditors: ChengWang
 * @LastEditTime: 2020-12-05 09:07:06
 * @FilePath: /note/cmake.md
-->
# cmake 

## way1: 检查c++编译器标志，设置c++11支持变量
  include(CheckCXXCompilerFlag)
  CHECK_CXX_COMPILER_FLAG("-std=c++11" COMPILER_SUPPORTS_CXX11)
  CHECK_CXX_COMPILER_FLAG("-std=c++0x" COMPILER_SUPPORTS_CXX0X)

###  使用变量设置编译标志
    if(COMPILER_SUPPORTS_CXX11)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
    elseif(COMPILER_SUPPORTS_CXX0X)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++0x")
    else()
    message(STATUS "The compiler ${CMAKE_CXX_COMPILER} has no C++11 support. Please use a different C++ compiler.")
    endif()

## way2:
  set(CMAKE_CXX_STANDARD 11)