cmake_minimum_required(VERSION 3.0.0)
project(sds VERSION 1.0.0)

option(BUILD_SHARED "Set to build this library as shared" OFF)

file(GLOB sds_headers ${CMAKE_SOURCE_DIR}/*.h)
file(GLOB sds_sources ${CMAKE_SOURCE_DIR}/*.c)

if(BUILD_SHARED)
    add_library(sds SHARED ${sds_sources} ${sds_headers})
else()
    add_library(sds STATIC ${sds_sources} ${sds_headers})
endif(BUILD_SHARED)

