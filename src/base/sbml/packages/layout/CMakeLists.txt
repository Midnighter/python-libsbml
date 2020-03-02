add_library(layout OBJECT
    sbml/ReactionGlyph.cpp
    sbml/Point.cpp
    sbml/GraphicalObject.cpp
    sbml/CompartmentGlyph.cpp
    sbml/Dimensions.cpp
    sbml/Curve.cpp
    sbml/Layout.cpp
    sbml/SpeciesGlyph.cpp
    sbml/ReferenceGlyph.cpp
    sbml/LineSegment.cpp
    sbml/GeneralGlyph.cpp
    sbml/CubicBezier.cpp
    sbml/BoundingBox.cpp
    sbml/SpeciesReferenceGlyph.cpp
    sbml/TextGlyph.cpp
    util/LayoutUtilities.cpp
    util/LayoutAnnotation.cpp
    validator/LayoutValidator.cpp
    validator/LayoutIdentifierConsistencyValidator.cpp
    validator/LayoutConsistencyValidator.cpp
    validator/constraints/LayoutIdentifierConsistencyConstraints.cpp
    validator/constraints/UniqueIdsLayout.cpp
    validator/constraints/LayoutConsistencyConstraints.cpp
    extension/LayoutModelPlugin.cpp
    extension/LayoutSpeciesReferencePlugin.cpp
    extension/LayoutSBMLDocumentPlugin.cpp
    extension/LayoutExtension.cpp
)

set_target_properties(layout PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(layout PRIVATE
    "${SRC}"
)
