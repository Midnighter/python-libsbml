add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/sbml")

add_library(sources OBJECT
    libsbml_wrap.cpp
    adler32.c
    blocksort.c
    bz_compress.c
    bzlib.c
    compress.c
    crc32.c
    crctable.c
    decompress.c
    deflate.c
    gzio.c
    huffman.c
    infback.c
    inffast.c
    inflate.c
    inftrees.c
    randtable.c
    trees.c
    uncompr.c
    xmlparse.c
    xmlrole.c
    xmltok.c
    xmltok_impl.c
    xmltok_ns.c
    zutil.c
    $<TARGET_OBJECTS:sbml_objects>
)

set_target_properties(sources PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_link_libraries(sources PRIVATE
    sbml_objects
    )

target_include_directories(sources PRIVATE
    "${SRC}"
    "${Python3_INCLUDE_DIRS}"
)
