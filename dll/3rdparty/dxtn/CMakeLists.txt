
spec2def(dxtn.dll dxtn.spec)

add_library(dxtn SHARED
    txc_compress_dxtn.c
    txc_fetch_dxtn.c
    ${CMAKE_CURRENT_BINARY_DIR}/dxtn.def)

set_entrypoint(dxtn 0)
add_importlibs(dxtn msvcrt)
add_cd_file(TARGET dxtn DESTINATION reactos/system32 FOR all)
