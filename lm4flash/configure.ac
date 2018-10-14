AC_INIT([lm4flash], 1.0)
AM_INIT_AUTOMAKE([foreign -Wall -Werror])
AC_PROG_CC
AC_CHECK_HEADER([libusb-1.0/libusb.h],
		[AC_CHECK_LIB([usb-1.0], [libusb_bulk_transfer],
			      [LIBS="$LIBS -lusb-1.0"],
			      [AC_MSG_ERROR([Missing libusb-1.0 library!])])],
[AC_MSG_ERROR([Missing libusb-1.0/libusb.h])])
AC_CONFIG_FILES(Makefile)
AC_OUTPUT
