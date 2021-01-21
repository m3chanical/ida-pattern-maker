cmake_minimum_required(VERSION 3.2 FATAL_ERROR)

project(ida-pattern-maker)

# Plugin 1
set(PLUGIN_NAME              ida-pattern-maker)
set(PLUGIN_SOURCES           Main.cpp)
set(PLUGIN_RUN_ARGS          "-t -z10000") # Debug messages for the debugger
include(${CMAKE_CURRENT_LIST_DIR}/plugins.cmake)
