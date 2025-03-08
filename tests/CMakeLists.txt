enable_testing()

add_subdirectory(filters)
add_test(NAME hello_test COMMAND hello_test)