cmake_minimum_required(VERSION 3.23)

project(cmake_test_bin LANGUAGES CXX)
add_executable(cmake_test_bin main.cpp)
target_link_libraries(cmake_test_bin PRIVATE cmake_test_lib_cxx cmake_test_lib_c)

add_subdirectory(interface-lib)
add_subdirectory(lib-c)
add_subdirectory(lib-cxx)
