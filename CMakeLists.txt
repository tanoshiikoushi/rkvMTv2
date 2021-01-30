cmake_minimum_required(VERSION 3.12)

include(CMakePackageConfigHelpers)

SET(curr_version 1.0)

project(rkvMTv2 VERSION ${curr_version} 
				DESCRIPTION "A rewrite of rkvMT"
				LANGUAGES CXX)
				
add_subdirectory(extern/libRKV1)
include_directories(${CMAKE_SOURCE_DIR}/extern/libRKV1/include)
add_subdirectory(src)