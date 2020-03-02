add_library(qual OBJECT
    sbml/Output.cpp
    sbml/Input.cpp
    sbml/DefaultTerm.cpp
    sbml/Transition.cpp
    sbml/QualitativeSpecies.cpp
    sbml/FunctionTerm.cpp
    validator/QualValidator.cpp
    validator/QualConsistencyValidator.cpp
    validator/QualIdentifierConsistencyValidator.cpp
    validator/QualMathConsistencyValidator.cpp
    validator/constraints/ResultBecomesNegative.cpp
    validator/constraints/QSAssignedOnce.cpp
    validator/constraints/ResultExceedsMaximum.cpp
    validator/constraints/QualCSymbolMathCheck.cpp
    validator/constraints/QualConsistencyConstraints.cpp
    validator/constraints/QualUniqueModelWideIds.cpp
    validator/constraints/QualIdentifierConsistencyConstraints.cpp
    validator/constraints/QualMathConsistencyConstraints.cpp
    extension/QualModelPlugin.cpp
    extension/QualSBMLDocumentPlugin.cpp
    extension/QualExtension.cpp
)

set_target_properties(qual PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(qual PRIVATE
    "${SRC}"
)
