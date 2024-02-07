AC_PREREQ([2.69])
AC_INIT([FULL-PACKAGE-NAME], [VERSION], [BUG-REPORT-ADDRESS])
AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_MACRO_DIRS([m4])
AM_INIT_AUTOMAKE([foreign subdir-objects]) # Does not require NEWS, COPYING, AUTHORS, ChangeLog or README

AM_SILENT_RULES([yes])

AC_PROG_CXX
AC_LANG([C++])
AC_PROG_CXX([$RTSCC c++ clang++])
AC_PROG_INSTALL
AX_CXX_COMPILE_STDCXX_17(ext,mandatory)

AC_CHECK_HEADER([rtapi.h hal.h i2c-dev.h])

AC_PREFIX_DEFAULT(run-in-place)
AC_PATH_PROG(GREP, grep)
AC_PATH_PROG(EGREP, egrep)


AC_CHECK_LIB([i2c], [i2c_smbus_write_quick],[],[
                 AC_MSG_ERROR([You need to install i2c library.])
                 ])


AC_CHECK_LIB([linuxcnchal], [hal_ready],[],[
                 AC_MSG_ERROR([You need to install i2c library.])
                 ])

AC_ENABLE_SHARED
AC_DISABLE_STATIC
LT_INIT([dlopen])
LTDL_INIT([nonrecursive])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
