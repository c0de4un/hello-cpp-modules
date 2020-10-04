# ------------------------------------------------------------------------------

# // ------------------------------------------------------------------------------
#
# Tutorial Project for C++ 20 Modules.
#
# License: see "LICENSE" file.
#
# // ------------------------------------------------------------------------------

# =================================================================================
# CMake Meta-Data
# =================================================================================

# CMake-Version
cmake_minimum_required ( VERSION 3.17 FATAL_ERROR )

# =================================================================================
# OPTIONS
# =================================================================================

include ( "cmake/options.cmake" )

# =================================================================================
# PROJECT
# =================================================================================

# Project Name
set ( PROJECT_NAME "hello_cpp_modules" )

# Project Version
set ( PROJECT_VERSION 0.0.1 )

# Project Description
set ( PROJECT_DESCRIPTION "C++ 20 Modules Samples Project" )

# C++ Version
set ( CMAKE_CXX_STANDARD 20 )
set ( CMAKE_CXX_STANDARD_REQUIRED ON )

# Configure Project
project ( ${PROJECT_NAME} VERSION ${PROJECT_VERSION} DESCRIPTION ${PROJECT_DESCRIPTION} LANGUAGES C CXX )

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

# =================================================================================
# CONFIGS
# =================================================================================

include ( "cmake/configs.cmake" )

# =================================================================================
# MODULES
# =================================================================================
message ( STATUS "CXX_STANDART=${CXX_STANDARD}" )
# Lib


# Executable
add_subdirectory ( "src/cpp/app" )

# ------------------------------------------------------------------------------
