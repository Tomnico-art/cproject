# cmake最低版本号要求
cmake_minimum_required(VERSION 3.0)
# 项目信息
project(CGAOJI)
# 头文件目录
include_directories(${CGAOJI_SOURCE_DIR}/include)
#库文件目录
link_directories(${CGAOJI_SOURCE_DIR}/lib)
# 查找当前目录下所有源文件，并将名称保存到DIR_SRCS变量
aux_source_directory(${CGAOJI_SOURCE_DIR}/src DIR_SRCS)
# 指定生成目标
add_executable(MyCgao ${DIR_SRCS})
# 引入math动态链接库
target_link_libraries(MyCgao -lMyMath)