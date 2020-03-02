add_library(extension OBJECT
    ASTBasePlugin.cpp
    SBaseExtensionPoint.cpp
    ISBMLExtensionNamespaces.cpp
    SBMLExtensionException.cpp
    SBMLDocumentPlugin.cpp
    SBasePluginCreatorBase.cpp
    SBasePlugin.cpp
    SBMLExtension.cpp
    SBMLDocumentPluginNotRequired.cpp
    SBMLExtensionNamespaces.cpp
    SBMLExtensionRegistry.cpp
)

set_target_properties(extension PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(extension PRIVATE
    "${SRC}"
)
