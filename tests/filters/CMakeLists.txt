add_executable(hello_test)

target_sources(
    hello_test
    PRIVATE hello_test.cpp
    PUBLIC FILE_SET
           HEADERS
           BASE_DIRS
           ${PROJECT_SOURCE_DIR}/include
           ${PROJECT_SOURCE_DIR}/external/googletest/googletest/include/
           FILES
           ${PROJECT_SOURCE_DIR}/include/audiotools/filters/hello.hpp
           ${PROJECT_SOURCE_DIR}/external/googletest/googletest/include/gtest/gtest.h
)

target_link_libraries(hello_test PRIVATE gtest_main)
