add_library(fbc OBJECT
    sbml/FbcAssociation.cpp
    sbml/FluxBound.cpp
    sbml/FbcAnd.cpp
    sbml/GeneProductAssociation.cpp
    sbml/Association.cpp
    sbml/GeneAssociation.cpp
    sbml/GeneProductRef.cpp
    sbml/FluxObjective.cpp
    sbml/Objective.cpp
    sbml/FbcOr.cpp
    sbml/GeneProduct.cpp
    util/FbcV1ToV2Converter.cpp
    util/FbcToCobraConverter.cpp
    util/CobraToFbcConverter.cpp
    util/FbcV2ToV1Converter.cpp
    validator/FbcValidator.cpp
    validator/FbcConsistencyValidator.cpp
    validator/FbcIdentifierConsistencyValidator.cpp
    validator/constraints/FbcConsistencyConstraints.cpp
    validator/constraints/UniqueGeneProductLabels.cpp
    validator/constraints/FluxBoundsConsistent.cpp
    validator/constraints/FbcIdentifierConsistencyConstraints.cpp
    validator/constraints/UniqueModelWideIds.cpp
    extension/FbcSBMLDocumentPlugin.cpp
    extension/FbcModelPlugin.cpp
    extension/FbcSpeciesPlugin.cpp
    extension/FbcExtension.cpp
    extension/FbcReactionPlugin.cpp
)

set_target_properties(fbc PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(fbc PRIVATE
    "${SRC}"
)
