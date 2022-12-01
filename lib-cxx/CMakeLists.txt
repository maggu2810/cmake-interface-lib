cmake_minimum_required(VERSION 3.23)
project(cmake_test_lib_cxx LANGUAGES CXX)
add_library(cmake_test_lib_cxx main.c)
target_link_libraries(cmake_test_lib_cxx INTERFACE cmake_test_interface_lib)
