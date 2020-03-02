add_library(multi OBJECT
    sbml/SpeciesFeatureType.cpp
    sbml/BindingSiteSpeciesType.cpp
    sbml/MultiSpeciesType.cpp
    sbml/SpeciesFeature.cpp
    sbml/CompartmentReference.cpp
    sbml/SpeciesTypeComponentMapInProduct.cpp
    sbml/SpeciesFeatureValue.cpp
    sbml/SpeciesTypeInstance.cpp
    sbml/SubListOfSpeciesFeatures.cpp
    sbml/OutwardBindingSite.cpp
    sbml/IntraSpeciesReaction.cpp
    sbml/PossibleSpeciesFeatureValue.cpp
    sbml/SpeciesTypeComponentIndex.cpp
    sbml/InSpeciesTypeBond.cpp
    validator/MultiMathMLConsistencyValidator.cpp
    validator/MultiIdentifierConsistencyValidator.cpp
    validator/MultiConsistencyValidator.cpp
    validator/MultiValidator.cpp
    validator/constraints/UniqueSFTIdsWithinMultiSpeciesType.cpp
    validator/constraints/UniqueCRefIdsWithinCompartment.cpp
    validator/constraints/MultiMathCiCheckSpeciesReference.cpp
    validator/constraints/MultiMathCiCheckRepresentationType.cpp
    validator/constraints/UniqueSTIIdsWithinMultiSpeciesType.cpp
    validator/constraints/UniqueSLOSFIdsWithinSpecies.cpp
    validator/constraints/UniqueMultiComponentIds.cpp
    validator/constraints/MultiConsistencyConstraints.cpp
    validator/constraints/MultiIdBase.cpp
    validator/constraints/MultiMathMLConsistencyConstraints.cpp
    validator/constraints/UniqueSTCIdsWithinMultiSpeciesType.cpp
    validator/constraints/UniqueISTBIdsWithinMultiSpeciesType.cpp
    validator/constraints/MultiIdentifierConsistencyConstraints.cpp
    validator/constraints/UniqueSpeciesFeatureIdsWithinSpecies.cpp
    validator/constraints/UniqueMultiIdBase.cpp
    extension/MultiModelPlugin.cpp
    extension/MultiExtension.cpp
    extension/MultiSpeciesReferencePlugin.cpp
    extension/MultiSimpleSpeciesReferencePlugin.cpp
    extension/MultiCompartmentPlugin.cpp
    extension/MultiListOfReactionsPlugin.cpp
    extension/MultiASTPlugin.cpp
    extension/MultiSBMLDocumentPlugin.cpp
    extension/MultiSpeciesPlugin.cpp
)

set_target_properties(multi PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(multi PRIVATE
    "${SRC}"
)
