add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/comp")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/fbc")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/groups")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/l3v2extendedmath")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/layout")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/multi")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/qual")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/render")

add_library(packages OBJECT
    $<TARGET_OBJECTS:comp>
    $<TARGET_OBJECTS:fbc>
    $<TARGET_OBJECTS:groups>
    $<TARGET_OBJECTS:l3v2extendedmath>
    $<TARGET_OBJECTS:layout>
    $<TARGET_OBJECTS:multi>
    $<TARGET_OBJECTS:qual>
    $<TARGET_OBJECTS:render>
)

set_target_properties(packages PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_link_libraries(packages PRIVATE
    comp
    fbc
    groups
    l3v2extendedmath
    layout
    multi
    qual
    render
    )

target_include_directories(packages PRIVATE
    "${SRC}"
)
