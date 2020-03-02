add_library(comp OBJECT
    sbml/Replacing.cpp
    sbml/ReplacedElement.cpp
    sbml/CompBase.cpp
    sbml/Port.cpp
    sbml/ListOfDeletions.cpp
    sbml/ReplacedBy.cpp
    sbml/ListOfExternalModelDefinitions.cpp
    sbml/Deletion.cpp
    sbml/ListOfReplacedElements.cpp
    sbml/ListOfModelDefinitions.cpp
    sbml/ListOfPorts.cpp
    sbml/SBaseRef.cpp
    sbml/ModelDefinition.cpp
    sbml/ListOfSubmodels.cpp
    sbml/Submodel.cpp
    sbml/ExternalModelDefinition.cpp
    util/SBMLResolver.cpp
    util/SBMLResolverRegistry.cpp
    util/SBMLFileResolver.cpp
    util/CompFlatteningConverter.cpp
    util/SBMLUri.cpp
    validator/CompIdentifierConsistencyValidator.cpp
    validator/CompConsistencyValidator.cpp
    validator/CompUnitConsistencyValidator.cpp
    validator/CompValidator.cpp
    validator/constraints/CompConsistencyConstraints.cpp
    validator/constraints/CompIdBase.cpp
    validator/constraints/UniqueCompIdBase.cpp
    validator/constraints/PackageIdReplacementCheck.cpp
    validator/constraints/ClassReplacements.cpp
    validator/constraints/CompUnitConsistencyConstraints.cpp
    validator/constraints/CompIdentifierConsistencyConstraints.cpp
    validator/constraints/UniquePortIds.cpp
    validator/constraints/ExtModelReferenceCycles.cpp
    validator/constraints/UniquePortReferences.cpp
    validator/constraints/UnitReplacementCheck.cpp
    validator/constraints/UniqueReplacedReferences.cpp
    validator/constraints/UniqueComponentIds.cpp
    validator/constraints/UniqueModelIds.cpp
    validator/constraints/SubmodelReferenceCycles.cpp
    extension/CompModelPlugin.cpp
    extension/CompSBMLDocumentPlugin.cpp
    extension/CompSBasePlugin.cpp
    extension/CompExtension.cpp
)

set_target_properties(comp PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(comp PRIVATE
    "${SRC}"
)
