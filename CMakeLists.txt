cmake_minimum_required(VERSION 2.8)

project(brute_force_bip38)

set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} "-std=c++11 -pthread")

add_executable(brute_force_bip38 src/main.cpp)
add_subdirectory(third_party/libwally-core)

target_link_libraries(brute_force_bip38 
    PRIVATE 
    libwally-core
)
