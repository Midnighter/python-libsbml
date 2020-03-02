add_library(units OBJECT
    FormulaUnitsData.cpp
    UnitFormulaFormatter.cpp
    UnitKindList.cpp
)

set_target_properties(units PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(units PRIVATE
    "${SRC}"
)
