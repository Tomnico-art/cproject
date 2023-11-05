# cmake最低版本号要求
cmake_minimum_required(VERSION 3.0)
# 项目信息
project(MYMATH)
# 头文件目录
include_directories(${MYMATH_SOURCE_DIR})
# 查找当前目录下所有源文件，并将名称保存到DIR_SRCS变量
aux_source_directory(${MYMATH_SOURCE_DIR} DIR_SRCS)
# 指定生成目标 SHARED生成动态库.so 不加生成静态库.a
add_library(MyMath SHARED ${DIR_SRCS})