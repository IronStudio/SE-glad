cmake_minimum_required(VERSION 3.26)


project(SE_glad)
set(SE_GLAD_INCLUDE_DIR ${PROJECT_SOURCE_DIR}/include)
file(GLOB_RECURSE se_glad_source_files ${PROJECT_SOURCE_DIR}/src/*.c)

add_library(glad STATIC ${se_glad_source_files})
target_include_directories(glad PUBLIC ${SE_GLAD_INCLUDE_DIR})