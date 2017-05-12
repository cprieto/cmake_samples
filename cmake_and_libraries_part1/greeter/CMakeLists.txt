cmake_minimum_required (VERSION 3.6)
project (libgreeter VERSION 1.0)

include_directories (${CMAKE_CURRENT_SOURCE_DIR}/includes)

set (GREETER_SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
set (GREETER_SOURCE ${GREETER_SOURCE_DIR}/greeter.c)

add_library (greeter SHARED ${GREETER_SOURCE})
add_library (greeter_static STATIC ${GREETER_SOURCE})

if (WIN32)
    set_target_properties (greeter_static PROPERTIES OUTPUT_NAME Greeter CLEAN_DIRECTORY_OUTPUT 1)
    set_target_properties (greeter PROPERTIES OUTPUT_NAME Greeter CLEAN_DIRECTORY_OUTPUT 1)
endif()

target_include_directories (greeter PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/includes)
