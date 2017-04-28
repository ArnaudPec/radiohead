AC_INIT([RadioHead], [1.50], [arnaud.pecoraro@smile.fr])
AC_PREREQ([2.59])
AC_CONFIG_SRCDIR([configure.ac])
AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_HEADERS([config.h])

AM_INIT_AUTOMAKE([1.6 dist-bzip2 -Wall -Werror foreign])
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

AC_SYS_LARGEFILE
AC_CANONICAL_BUILD
AC_CANONICAL_HOST

AC_PROG_CC
AC_PROG_CXX
AX_CXX_COMPILE_STDCXX_11
AM_PROG_AR

LT_INIT
AC_ENABLE_SHARED

PKG_PROG_PKG_CONFIG

AC_SEARCH_LIBS([wiringPiSetup], [wiringPi], [HAVE_WIRINGPI=1], [HAVE_WIRINGPI=0])

if test  $HAVE_WIRINGPI = 0; then
    AC_MSG_ERROR(WiringPi library not found!)
fi

AC_CONFIG_FILES([
Makefile
radiohead.pc
])

AC_OUTPUT

echo
echo
echo
echo
echo "------------------------------------------------------------------------"
echo "$PACKAGE $VERSION"
echo "------------------------------------------------------------------------"
echo
echo
echo "Configuration Options Summary:"
echo
echo "Compilation............: make (or gmake)"
echo "  CPPFLAGS.............: $CPPFLAGS"
echo "  CFLAGS...............: $CFLAGS"
echo "  LDFLAGS..............: $LDFLAGS"
echo
echo "Installation...........: make install (as root if needed, with 'su' or 'sudo')"
echo "  prefix...............: $prefix"
echo
