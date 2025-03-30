add_library(wwlib STATIC
    b64pipe.cpp
    b64straw.cpp
    base64.cpp
    buff.cpp
    bufffile.cpp
    chunkio.cpp
    cpudetect.cpp
    crc.cpp
    cstraw.cpp
    ffactory.cpp
    gcd_lcm.cpp
    hash.cpp
    ini.cpp
    int.cpp
    mpmath.cpp
    mpu.cpp
    multilist.cpp
    mutex.cpp
    nstrdup.cpp
    pipe.cpp
    pk.cpp
    random.cpp
    rawfile.cpp
    readline.cpp
    realcrc.cpp
    refcount.cpp
    registry.cpp
    slnode.cpp
    straw.cpp
    strtok_r.cpp
    systimer.cpp
    TARGA.cpp
    textfile.cpp
    thread.cpp
    trim.cpp
    vector.cpp
    widestring.cpp
    #wwfile.cpp
    wwstring.cpp
    xpipe.cpp
    xstraw.cpp
    #xsurface.cpp

    # (Optional) If you want headers visible in IDEs:
    # always.h
    # argv.h
    # b64pipe.h
    # ...
    # xsurface.h
    # _mono.h
)

set_target_properties(wwlib PROPERTIES
    ${GNG_GLOBAL_PROPERTIES}
 )

target_include_directories(wwlib PRIVATE
    "${CMAKE_CURRENT_SOURCE_DIR}/../wwdebug"
)

target_compile_definitions(wwlib PRIVATE
    ${GNG_COMPILE_DEFINITIONS}
    WIN32_LEAN_AND_MEAN
    REGEX_MALLOC
    STDC_HEADERS
)

target_compile_options(wwlib PRIVATE
    ${GNG_COMPILE_OPTIONS}
)

target_link_options(wwlib PRIVATE
    ${GNG_LINK_OPTIONS}
)
