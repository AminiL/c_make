cmake_minimum_required(VERSION 3.10)

project(TP_CMAKE)

set(SOURCE ${CMAKE_DIR}/B/main.cpp)


execute_process(
WORKING_DIRECTORY A
COMMAND ${PYTHON_EXECUTABLE} script.py
)

include_directories(${CMAKE_DIR})

add_executable(result ${SOURCE})