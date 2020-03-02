add_library(compress OBJECT
    InputDecompressor.cpp
    unzip.c
    OutputCompressor.cpp
    zipfstream.cpp
    bzfstream.cpp
    CompressCommon.cpp
    zip.c
    zfstream.cpp
    ioapi_mem.c
    ioapi.c
    iowin32.c
)

set_target_properties(compress PROPERTIES
    POSITION_INDEPENDENT_CODE ON
    )

target_include_directories(compress PRIVATE
    "${SRC}"
)
