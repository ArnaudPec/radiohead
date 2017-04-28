ACLOCAL_AMFLAGS= -I m4
lib_LTLIBRARIES=libradiohead.la

AM_CXXFLAGS = \
-I. \
 -DRH_PLATFORM=RH_PLATFORM_RPI -D__RASPBERRY_PI_\
-DPACKAGE_BIN_DIR=\"$(bindir)\" \
-DPACKAGE_LIB_DIR=\"$(libdir)\" \
@CFLAGS@

pkginclude_HEADERS= \
RHLinuxSPI.h \
RH_ASK.h \
RHCRC.h \
RHDatagram.h \
RHGenericDriver.h \
RHGenericSPI.h \
RHSoftwareSPI.h \
RH_NRF51.h \
RH_RF69.h \
RH_RF95.h \
RadioHead.h \
RH_TCP.h

libradiohead_la_SOURCES= \
RH_ASK.cpp \
RHCRC.cpp \
RHDatagram.cpp \
RHGenericDriver.cpp \
RHGenericSPI.cpp \
RHSoftwareSPI.cpp \
RHLinuxSPI.cpp \
RH_NRF51.cpp \
RH_RF69.cpp \
RH_RF95.cpp \
RH_TCP.cpp

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = radiohead.pc
