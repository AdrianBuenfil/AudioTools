cmake_minimum_required(VERSION 3.28)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_COMPILER clang++-18)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

project(AudioTools CXX)

find_program(CLANG_TIDY_PATH clang-tidy REQUIRED)
set(CMAKE_CXX_CLANG_TIDY ${CLANG_TIDY_PATH};-checks=*)

find_program(CPPCHECK_PATH cppcheck REQUIRED)
set(CMAKE_CXX_CPPCHECK ${CPPCHECK_PATH} --enable=all)

add_subdirectory(apps)
add_subdirectory(external)
add_subdirectory(source)
add_subdirectory(tests)

enable_testing()