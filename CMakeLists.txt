# CMake最低版本要求
cmake_minimum_required(VERSION 3.10)

# 项目名称和版本
project(MyProject VERSION 1.0)

# 设置C++标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# 包含目录
include_directories(${PROJECT_SOURCE_DIR}/include)

# 查找源文件
file(GLOB_RECURSE SRC_FILES ${PROJECT_SOURCE_DIR}/src/*.cpp)

# 添加可执行文件
add_executable(MyExecutable ${SRC_FILES})

# 链接库（如果有）
# target_link_libraries(MyExecutable libmodule1 libmodule2)

# 添加测试（如果有）
enable_testing()
add_subdirectory(test)