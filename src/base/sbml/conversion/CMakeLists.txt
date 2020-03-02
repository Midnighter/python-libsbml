add_library(conversion OBJECT
    SBMLUnitsConverter.cpp
    SBMLIdConverter.cpp
    SBMLReactionConverter.cpp
    SBMLFunctionDefinitionConverter.cpp
    SBMLLocalParameterConverter.cpp
    SBMLStripPackageConverter.cpp
    SBMLRuleConverter.cpp
    ConversionOption.cpp
    SBMLLevelVersionConverter.cpp
    RegisterConverters.cpp
    SBMLRateOfConverter.cpp
    SBMLInferUnitsConverter.cpp
    ConversionProperties.cpp
    SBMLLevel1Version1Converter.cpp
    SBMLInitialAssignmentConverter.cpp
    SBMLConverter.cpp
    SBMLConverterRegistry.cpp
)

set_target_properties(conversion PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(conversion PRIVATE
    "${SRC}"
)
