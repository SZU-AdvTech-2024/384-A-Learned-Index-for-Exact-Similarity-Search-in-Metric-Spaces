# CMake最低版本要求
cmake_minimum_required(VERSION 3.10)

# 项目名称
project(LIMS)

# 设置C++标准为C++17
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# 添加编译选项
#add_compile_options(-Wall -O3 -ffast-math -march=native)
add_compile_options(-Wall)

# 设置构建类型为Debug
set(CMAKE_BUILD_TYPE "Debug")

# 查找所有的源文件
file(GLOB_RECURSE SOURCES "*.cpp")

file(GLOB_RECURSE REMOVE_CMAKE "${CMAKE_CURRENT_SOURCE_DIR}/build/*")
list(REMOVE_ITEM SOURCES ${REMOVE_CMAKE})

# 添加可执行文件
add_executable(${PROJECT_NAME} ${SOURCES})