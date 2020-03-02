add_library(render OBJECT
    sbml/RenderGroup.cpp
    sbml/LinearGradient.cpp
    sbml/RenderCurve.cpp
    sbml/ListOfGradientStops.cpp
    sbml/GlobalRenderInformation.cpp
    sbml/GradientBase.cpp
    sbml/Polygon.cpp
    sbml/ListOfDrawables.cpp
    sbml/ListOfGlobalStyles.cpp
    sbml/ListOfGradientDefinitions.cpp
    sbml/ListOfLineEndings.cpp
    sbml/Transformation2D.cpp
    sbml/Style.cpp
    sbml/ListOfColorDefinitions.cpp
    sbml/ListOfLocalStyles.cpp
    sbml/LineEnding.cpp
    sbml/Image.cpp
    sbml/RenderInformationBase.cpp
    sbml/LocalStyle.cpp
    sbml/RadialGradient.cpp
    sbml/RenderPoint.cpp
    sbml/ColorDefinition.cpp
    sbml/LocalRenderInformation.cpp
    sbml/Transformation.cpp
    sbml/ListOfCurveElements.cpp
    sbml/GraphicalPrimitive1D.cpp
    sbml/Rectangle.cpp
    sbml/Text.cpp
    sbml/ListOfGlobalRenderInformation.cpp
    sbml/RelAbsVector.cpp
    sbml/GraphicalPrimitive2D.cpp
    sbml/Ellipse.cpp
    sbml/DefaultValues.cpp
    sbml/GlobalStyle.cpp
    sbml/ListOfLocalRenderInformation.cpp
    sbml/GradientStop.cpp
    sbml/RenderCubicBezier.cpp
    util/RenderUtilities.cpp
    util/RenderLayoutConverter.cpp
    validator/RenderValidator.cpp
    validator/RenderConsistencyValidator.cpp
    validator/RenderIdentifierConsistencyValidator.cpp
    validator/constraints/RenderIdentifierConsistencyConstraints.cpp
    validator/constraints/RenderConsistencyConstraints.cpp
    extension/RenderLayoutPlugin.cpp
    extension/RenderSBMLDocumentPlugin.cpp
    extension/RenderListOfLayoutsPlugin.cpp
    extension/RenderExtension.cpp
    extension/RenderGraphicalObjectPlugin.cpp
)

set_target_properties(render PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(render PRIVATE
    "${SRC}"
)
