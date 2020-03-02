add_library(l3v2extendedmath OBJECT
    validator/L3v2extendedmathUnitConsistencyValidator.cpp
    validator/L3v2extendedmathValidator.cpp
    validator/L3v2extendedmathMathMLConsistencyValidator.cpp
    validator/constraints/L3v2EMArgumentsUnitsCheck.cpp
    validator/constraints/L3v2extendedmathMathMLConsistencyConstraints.cpp
    validator/constraints/L3v2EMNumberArgsMathCheck.cpp
    validator/constraints/L3v2extendedmathUnitConsistencyConstraints.cpp
    extension/L3v2extendedmathASTPlugin.cpp
    extension/L3v2extendedmathExtension.cpp
    extension/L3v2extendedmathSBMLDocumentPlugin.cpp
)

set_target_properties(l3v2extendedmath PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(l3v2extendedmath PRIVATE
    "${SRC}"
)
