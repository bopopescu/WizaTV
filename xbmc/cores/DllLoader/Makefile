CFLAGS   += -DAPI_DEBUG
CXXFLAGS += -DAPI_DEBUG

SRCS  = coff.cpp
SRCS += dll.cpp
SRCS += DllLoader.cpp
SRCS += DllLoaderContainer.cpp
SRCS += dll_tracker.cpp
SRCS += dll_tracker_file.cpp
SRCS += dll_tracker_library.cpp
SRCS += dll_util.cpp
SRCS += LibraryLoader.cpp
SRCS += mmap_anon.c
SRCS += SoLoader.cpp

ifneq ($(findstring freebsd,arm-osx),freebsd)
SRCS += ldt_keeper.c
endif

LIB = dllloader.a

include /Users/osx/Desktop/kodi/xbmc/Makefile.include
-include $(patsubst %.cpp,%.P,$(patsubst %.c,%.P,$(SRCS)))
