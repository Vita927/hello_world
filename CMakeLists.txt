cmake_minimum_required(VERSION 3.4)
project(hello_world)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(FORMATTER_EX_PATH ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib)

add_executable(hello_world ${CMAKE_CURRENT_SOURCE_DIR}/hello_world.cpp)

add_subdirectory(${FORMATTER_EX_PATH} ${CMAKE_BINARY_DIR}/formatter_ex_lib)

target_link_libraries(hello_world formatter_ex)
