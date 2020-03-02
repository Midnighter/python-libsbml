add_library(groups OBJECT
    sbml/Group.cpp
    sbml/ListOfMembers.cpp
    sbml/Member.cpp
    sbml/ListOfGroups.cpp
    validator/GroupsIdentifierConsistencyValidator.cpp
    validator/GroupsValidator.cpp
    validator/GroupsConsistencyValidator.cpp
    validator/constraints/LOMembersConsistentReferences.cpp
    validator/constraints/GroupsIdentifierConsistencyConstraints.cpp
    validator/constraints/GroupCircularReferences.cpp
    validator/constraints/GroupsConsistencyConstraints.cpp
    validator/constraints/GroupsUniqueModelWideIds.cpp
    extension/GroupsExtension.cpp
    extension/GroupsSBMLDocumentPlugin.cpp
    extension/GroupsModelPlugin.cpp
)

set_target_properties(groups PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(groups PRIVATE
    "${SRC}"
)
