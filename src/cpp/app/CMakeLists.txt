# =================================================================================
# CMake Meta-Data
# =================================================================================

# CMake-Version
cmake_minimum_required ( VERSION 3.17 FATAL_ERROR )

# =================================================================================
# PROJECT
# =================================================================================

# Project Name
set ( PROJECT_NAME "hello_cpp_modules.app" )

# Project Version
set ( PROJECT_VERSION 0.0.1 )

# Project Description
set ( PROJECT_DESCRIPTION "C++ 20 Modules Samples Project" )

# Configure Project
project ( ${PROJECT_NAME} VERSION ${PROJECT_VERSION} DESCRIPTION ${PROJECT_DESCRIPTION} LANGUAGES C CXX )

# C++ Version
set ( CMAKE_CXX_STANDARD 20 )
set ( CMAKE_CXX_STANDARD_REQUIRED ON )

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

# =================================================================================
# SOURCES
# =================================================================================

set ( APP_SOURCES
    "main.cpp" )

# =================================================================================
# RESOURCES
# =================================================================================

set ( APP_RESOURCES "${CMAKE_SOURCE_DIR}/res/win/win_res.rc" )

# =================================================================================
# BUILD
# =================================================================================

add_executable ( hello_modules ${APP_SOURCES} "" ${APP_RESOURCES} )

# ------------------------------------------------------------------------------
