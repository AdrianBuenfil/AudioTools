add_library(HelloModule OBJECT)

target_sources(
    HelloModule
    PRIVATE hello.cpp
    PUBLIC FILE_SET HEADERS BASE_DIRS ${PROJECT_SOURCE_DIR}/include FILES
           ${PROJECT_SOURCE_DIR}/include/audiotools/filters/hello.hpp
)

add_test(NAME hello_tests COMMAND hello_tests)
