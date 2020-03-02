add_library(util OBJECT
    CallbackRegistry.cpp
    ElementFilter.cpp
    IdFilter.cpp
    IdList.cpp
    IdentifierTransformer.cpp
    List.cpp
    MathFilter.cpp
    MetaIdFilter.cpp
    PrefixTransformer.cpp
    Stack.c
    StringBuffer.c
    memory.c
    util.cpp
)

set_target_properties(util PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(util PRIVATE
    "${SRC}"
)
