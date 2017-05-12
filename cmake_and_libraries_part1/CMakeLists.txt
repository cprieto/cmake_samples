cmake_minimum_required (VERSION 3.6)
project (hello VERSION 1.0)

set (LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/output)
set (EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/output)

add_subdirectory (greeter)
add_subdirectory (hello_app)
