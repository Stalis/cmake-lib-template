cmake_minimum_required(VERSION 3.13)
project(lib C)

set(CMAKE_C_STANDARD 99)

file(GLOB SOURCES src/*.c)
file(GLOB HEADERS include/*.h)

add_library(lib SHARED ${SOURCES} ${HEADERS})
target_include_directories(lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)