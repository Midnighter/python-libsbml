add_library(xml OBJECT
    ExpatAttributes.cpp
    ExpatHandler.cpp
    ExpatParser.cpp
    XMLAttributes.cpp
    XMLBuffer.cpp
    XMLConstructorException.cpp
    XMLError.cpp
    XMLErrorLog.cpp
    XMLFileBuffer.cpp
    XMLHandler.cpp
    XMLInputStream.cpp
    XMLLogOverride.cpp
    XMLMemoryBuffer.cpp
    XMLNamespaces.cpp
    XMLNode.cpp
    XMLOutputStream.cpp
    XMLParser.cpp
    XMLToken.cpp
    XMLTokenizer.cpp
    XMLTriple.cpp
)

set_target_properties(xml PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(xml PRIVATE
    "${SRC}"
)
