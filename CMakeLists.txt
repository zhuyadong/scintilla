file(GLOB SCI_SRCS src/*.cxx fltk/*.cxx)
FL_ADD_LIBRARY(fltk_scintilla STATIC "${SCI_SRCS}")
if(OPTION_BUILD_SHARED_LIBS)
    FL_ADD_LIBRARY(fltk_scintilla SHARED "${SCI_SRCS}")
endif()

target_include_directories(fltk_scintilla PRIVATE
        include
        fltk
        lexlib
        src
)
