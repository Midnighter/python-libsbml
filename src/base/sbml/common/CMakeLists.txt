add_library(common OBJECT
    libsbml-version.cpp
    operationReturnValues.cpp
)

set_target_properties(common PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(common PRIVATE
    "${SRC}"
)
