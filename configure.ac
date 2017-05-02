#-----------------------------------------------------------------------------
# Pre-Conf
#-----------------------------------------------------------------------------

AC_PREREQ(2.59)

#-----------------------------------------------------------------------------
# Programs
#-----------------------------------------------------------------------------
AC_INIT([filewatcher], [1.1.0])
AC_CONFIG_MACRO_DIR([m4])

AM_INIT_AUTOMAKE([1.11 foreign parallel-tests])

AC_PROG_CC
AC_PROG_CXX
AC_PROG_INSTALL
AC_PROG_LIBTOOL

#-----------------------------------------------------------------------------
# Checks
#-----------------------------------------------------------------------------

# Checks for header files.
AC_HEADER_STDC
AC_CHECK_HEADERS([stdio.h stdlib.h sys/time.h])
AC_CHECK_HEADERS([string vector sstream fstream])

# Checks for typedefs, structures, and compiler characteristics.
AC_HEADER_STDBOOL
AC_C_CONST
AC_C_INLINE
AC_TYPE_SIZE_T

AX_CXX_COMPILE_STDCXX_11([noext])

METNO_PROG_PKG_CONFIG
METNO_REQUIRE_PKGS([PC], [
  metlibs-milogger >= 6.0.0
  metlibs-putools >= 7.0.0
  metlibs-qutilities-qt5 >= 8.0.0
  metlibs-coserver-qt5 >= 3.0.0
  Qt5Core Qt5Network
 ])
METNO_CHECK_QT5_TOOLS()



AC_OUTPUT(Makefile src/Makefile)
