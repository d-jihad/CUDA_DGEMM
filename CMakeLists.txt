cmake_minimum_required(VERSION 3.18)
project(CUDA_DGEMM)

find_package(CUDA QUIET REQUIRED)
enable_language(CUDA)

include_directories(${CUDA_INCLUDE_DIRS} include)

file(GLOB PROJECT_SOURCE_FILES src/*)
file(GLOB PROJECT_INCLUDE_FILES include/*)

add_executable(${PROJECT_NAME} ${PROJECT_SOURCE_FILES} ${PROJECT_INCLUDE_FILES})
