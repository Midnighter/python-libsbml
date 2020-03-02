add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/common")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/annotation")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/compress")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/conversion")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/extension")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/math")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/packages")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/units")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/util")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/validator")
add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/xml")

add_library(sbml_objects OBJECT
    $<TARGET_OBJECTS:common>
    $<TARGET_OBJECTS:annotation>
    $<TARGET_OBJECTS:compress>
    $<TARGET_OBJECTS:conversion>
    $<TARGET_OBJECTS:extension>
    $<TARGET_OBJECTS:math>
    $<TARGET_OBJECTS:packages>
    $<TARGET_OBJECTS:units>
    $<TARGET_OBJECTS:util>
    $<TARGET_OBJECTS:validator>
    $<TARGET_OBJECTS:xml>
    AlgebraicRule.cpp
    AssignmentRule.cpp
    Compartment.cpp
    CompartmentType.cpp
    Constraint.cpp
    Delay.cpp
    Event.cpp
    EventAssignment.cpp
    ExpectedAttributes.cpp
    FunctionDefinition.cpp
    InitialAssignment.cpp
    KineticLaw.cpp
    ListOf.cpp
    LocalParameter.cpp
    Model.cpp
    ModifierSpeciesReference.cpp
    Parameter.cpp
    Priority.cpp
    RateRule.cpp
    Reaction.cpp
    Rule.cpp
    SBMLConstructorException.cpp
    SBMLConvert.cpp
    SBMLDocument.cpp
    SBMLError.cpp
    SBMLErrorLog.cpp
    SBMLNamespaces.cpp
    SBMLReader.cpp
    SBMLTransforms.cpp
    SBMLTypeCodes.cpp
    SBMLVisitor.cpp
    SBMLWriter.cpp
    SBO.cpp
    SBase.cpp
    SimpleSpeciesReference.cpp
    Species.cpp
    SpeciesReference.cpp
    SpeciesType.cpp
    StoichiometryMath.cpp
    SyntaxChecker.cpp
    Trigger.cpp
    Unit.cpp
    UnitDefinition.cpp
    UnitKind.c
)

set_target_properties(sbml_objects PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_link_libraries(sbml_objects PRIVATE
    common
    annotation
    compress
    conversion
    extension
    math
    packages
    units
    util
    validator
    xml
    )


target_include_directories(sbml_objects PRIVATE
    "${SRC}"
)
