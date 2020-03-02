add_library(math OBJECT
    L3Parser.cpp
    FormulaFormatter.cpp
    L3ParserSettings.cpp
    L3FormulaFormatter.cpp
    MathML.cpp
    ASTNode.cpp
    FormulaTokenizer.cpp
    DefinitionURLRegistry.cpp
    FormulaParser.cpp
)

set_target_properties(math PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(math PRIVATE
    "${SRC}"
)
