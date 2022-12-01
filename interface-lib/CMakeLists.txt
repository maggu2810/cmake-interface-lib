cmake_minimum_required(VERSION 3.23)
project(cmake_test_interface_lib)
add_library(cmake_test_interface_lib INTERFACE)

target_link_options(cmake_test_interface_lib INTERFACE
    $<$<OR:$<LINK_LANG_AND_ID:C,GNU>,$<LINK_LANG_AND_ID:CXX,GNU>>:-Wl,--no-undefined>
    $<$<OR:$<LINK_LANG_AND_ID:C,Clang>,$<LINK_LANG_AND_ID:CXX,Clang>>:-Wl,-undefined,error>
    )

target_compile_options(cmake_test_interface_lib INTERFACE
    -Werror=switch)

target_compile_features(cmake_test_interface_lib INTERFACE c_std_17 cxx_std_17)
