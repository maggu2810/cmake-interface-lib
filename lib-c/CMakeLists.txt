cmake_minimum_required(VERSION 3.23)
project(cmake_test_lib_c LANGUAGES C)
add_library(cmake_test_lib_c main.c)
target_link_libraries(cmake_test_lib_c INTERFACE cmake_test_interface_lib)
