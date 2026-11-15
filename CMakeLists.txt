cmake_minimum_required(VERSION 4.3.0)
project(catalyst C CXX)
set_property(GLOBAL PROPERTY USE_FOLDERS ON)
include_directories("${CMAKE_SOURCE_DIR}/include")
include(${CMAKE_SOURCE_DIR}/cmake/CMakeInit.cmake REQUIRED)
metadata("catalyst" 1 0 0 "alpha.1" "C ABI implementation of the CatalystUI model.")
configure("${TARGET_VENDOR}" "${TARGET_SYSTEM}" "${TARGET_ARCHITECTURE}")
define("cmake/CMakeConfig.h" "cmakecfg.h")

# DARWIN platform specifics
if(TARGET_PLATFORM_DARWIN)
    # Enable Objective-C and Objective-C++
    enable_language(OBJC OBJCXX)
endif()
