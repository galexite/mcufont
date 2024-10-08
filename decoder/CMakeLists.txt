add_library(mcufont_decoder STATIC
    mf_bwfont.c
    mf_bwfont.h
    mf_config.h
    mf_encoding.c
    mf_encoding.h
    mf_font.c
    mf_font.h
    mf_justify.c
    mf_justify.h
    mf_kerning.c
    mf_kerning.h
    mf_rlefont.c
    mf_rlefont.h
    mf_scaledfont.c
    mf_scaledfont.h
    mf_wordwrap.c
    mf_wordwrap.h
)

target_include_directories(mcufont_decoder PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

set_target_properties(mcufont_decoder
  PROPERTIES
    C_STANDARD 99
    C_STANDARD_REQUIRED ON
)

add_library(mcufont::decoder ALIAS mcufont_decoder)
