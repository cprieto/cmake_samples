cmake_minimum_required (VERSION 3.5)
project (HelloCMake)

set (PROJECT_SOURCE_DIR ${CMAKE_SOURCE_DIR}/src)
set (HELLO_SOURCES ${PROJECT_SOURCE_DIR}/hello.c)
set (GREETER_SOURCES ${PROJECT_SOURCE_DIR}/greeter.c)

# These are the corresponding output paths
set (EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/output)
set (LIBRARY_OUTPUT_PATH ${EXECUTABLE_OUTPUT_PATH})

add_executable (hello ${HELLO_SOURCES})
add_library (greeter STATIC ${GREETER_SOURCES})
target_link_libraries (hello greeter)
