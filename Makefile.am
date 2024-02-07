AM_CFLAGS        = -I$(top_srcdir)
AM_CPPFLAGS      = -I$(top_srcdir) -I/usr/include/linuxcnc
ACLOCAL_AMFLAGS  = -I m4

# Convenience library so that it can be resued
# between my_executable and the tests
lib_LTLIBRARIES          = hal_mcp23017.la

hal_mcp23017_sodir       = /usr/lib/linuxcnc/modules/
hal_mcp23017_so_SOURCES  = "hal_mcp23017.cpp mcp23017.cpp" 
hal_mcp23017_so_HEADERS  = "hal_mcp23017.h mcp23017.h" 
hal_mcp23017_so_CXXFLAGS = $(AM_CPPFLAGS) $(CODE_COVERAGE_CFLAGS) --std=c11 -fPIC -O2
hal_mcp23017_so_LDADD    = -li2c -llinuxcnchal
hal_mcp23017_so_INST
