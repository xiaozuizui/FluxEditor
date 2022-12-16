set(littleEngine_VERSION "0.1")
cmake_minimum_required(VERSION 3.15.7)
project(
    littleEngine
    VERSION ${littleEngine_VERSION})

if ( CMAKE_SYSTEM_NAME MATCHES "Windows" )
    set( std "/std:" )
else()
    set( std "-std=" )
endif()

set( basic_cxx17 "c++17" )
set( str_cxx17 "${std}${basic_cxx17}")
include( CheckCXXCompilerFlag )
check_cxx_compiler_flag( "${str_cxx17}" _cpp_17_flag_supported )
if (_cpp_17_flag_supported )
    set(CMAKE_CXX_STANDARD 17 )    
endif()

add_subdirectory("3rd") 



add_subdirectory("src/core")