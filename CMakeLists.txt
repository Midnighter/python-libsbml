cmake_minimum_required(VERSION 3.12)

project(sbml VERSION 5.18.1)

#set(CMAKE_CXX_STANDARD 11)
#set(CMAKE_CXX_STANDARD_REQUIRED True)
#set(CMAKE_CXX_FLAGS "-Wno-deprecated-register" )
set(CMAKE_C_FLAGS_DEBUG "-Wsign-compare -g -fwrapv -Wall -Wstrict-prototypes")
set(CMAKE_C_FLAGS_RELEASE "-Wsign-compare -DNDEBUG -g -fwrapv -O3 -Wall -Wstrict-prototypes")
set(CMAKE_CXX_FLAGS_DEBUG "-g -fwrapv -Wall")
set(CMAKE_CXX_FLAGS_RELEASE "-DNDEBUG -g -fwrapv -O3 -Wall")

################################################################################
# External Dependencies
################################################################################

find_package(Python3 COMPONENTS Interpreter Development)
if(Python3_FOUND)
    message("Python 3 interpreter: '${Python3_EXECUTABLE}'.")
    message("Python 3 include directory: '${Python3_INCLUDE_DIRS}'.")
else()
    message(SEND_ERROR "Python 3 not found!")
endif()

################################################################################
# Build Targets
################################################################################

add_compile_definitions(
    USE_COMP
    USE_QUAL
    USE_FBC
    USE_LAYOUTS
    USE_GROUPS
    USE_MULTI
    USE_RENDER
    USE_L3V2EXTENDEDMATH
    BZIP2_STATIC
    HAVE_MEMMOVE
    _LIB
    USE_EXPAT
    USE_ZLIB
    USE_BZ2
    )

set(SRC "${PROJECT_SOURCE_DIR}/src/base")
add_subdirectory("${SRC}")

add_library(sbml SHARED
    $<TARGET_OBJECTS:sources>
    )

set_target_properties(sbml PROPERTIES
    VERSION ${PROJECT_VERSION}
    POSITION_INDEPENDENT_CODE ON
    )

target_link_libraries(sbml PUBLIC
    sources
    )

target_include_directories(sbml PUBLIC
    $<BUILD_INTERFACE:"${SRC}">
    )

if(${CMAKE_SYSTEM_NAME} STREQUAL "Windows")
    add_compile_definitions(
        WIN32
        LIBSBML_EXPORTS
        LIBLAX_STATIC
    )
elseif(${CMAKE_SYSTEM_NAME} STREQUAL "Darwin")
    add_compile_definitions(DARWIN)
elseif(${CMAKE_SYSTEM_NAME} STREQUAL "Linux")
    add_compile_definitions(LINUX)
else()
    message(SEND_ERROR "Unsupported platform ${CMAKE_SYSTEM_NAME}.")
endif()

install(TARGETS sbml LIBRARY DESTINATION "${PROJECT_SOURCE_DIR}/src/libsbml")
