add_library(annotation OBJECT
    CVTerm.cpp
    Date.cpp
    RDFAnnotationParser.cpp
    ModelHistory.cpp
    ModelCreator.cpp
)

set_target_properties(annotation PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(annotation PRIVATE
    "${SRC}"
)
