EXTRA_DIST = \
	usb_linux.c \
	util_linux.c \
	usb_windows.c \
	util_windows.c \
	zlib-1.2.3-lib \
	prebuilt \
	usb \
	NOTICE

SUBDIRS = libzipfile

# introduced for libtool
ACLOCAL_AMFLAGS = -I m4

bin_PROGRAMS = prekit usbtest

# usb_os.c and util_os.c are links to platform specific source files
prekit_SOURCES = \
	protocol.c \
	engine.c \
	fastboot.c \
	fastboot.h \
	parser.c \
	parser.h \
	usb_os.c \
	util_os.c \
	usb.h

AM_CFLAGS = \
	@USB_INCLUDE@

prekit_LDADD = \
	$(top_builddir)/libzipfile/libzipfile.la \
	@ZLIB_LIBS@ \
	@USB_LIBS@

usbtest_SOURCES = \
	usbtest.c \
	usb_os.c

usbtest_LDADD = \
	@USB_LIBS@
