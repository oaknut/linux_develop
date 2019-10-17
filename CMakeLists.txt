#1.CMake最低版本要求
cmake_minimum_required (VERSION 2.8)

#CMakeLists.txt使用C++11标准
#add_definitions(-std=c++11)

#2.项目信息,指定项目的名称
project (main)

#3.头文件目录
#INCLUDE_DIRECTORIES(
#	include
#	)

#4.查找当前目录下的所有源文件
#并将名称保存到DIR_SRCS变量
aux_source_directory(. DIR_SRCS)

#5.设置环境变量：编译用到的源文件全部放到这里，否则编译能过，但执行会报错
#SET（TEST_MATH
#${DIR_SRCS}
#）

#6.指定生成目标
add_executable(main ${DIR_SRCS})

#7.添加可执行文件所需要的库，比如用到了libm.so（命名规则：lib+name+.so），就添加该库的名称
#TARGET_LINK_LIBRARIES(${PROJECT_NAME} m)

