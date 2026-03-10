EXTRA_DIST = \
		README \
		CHANGES \
		COPYING \
		BUGS \
		AUTHORS \
		Makefile.mingw

pkgdir = $(libdir)/purple-$(PURPLE_MAJOR_VERSION)

OSCARSOURCES = \
	admin.c        \
	adverts.c      \
	aim.h          \
	aim_cbtypes.h  \
	aim_internal.h \
	auth.c         \
	bart.c         \
	bos.c          \
	bstream.c      \
	buddylist.c    \
	chat.c         \
	chatnav.c      \
	conn.c         \
	email.c        \
	faimconfig.h   \
	ft.c           \
	icq.c          \
	im.c           \
	invite.c       \
	locate.c       \
	misc.c         \
	msgcookie.c    \
	odir.c         \
	popups.c       \
	rxhandlers.c   \
	rxqueue.c      \
	search.c       \
	service.c      \
	snac.c         \
	ssi.c          \
	stats.c        \
	tlv.c          \
	translate.c    \
	txqueue.c      \
	util.c         \
	oscar.c

AM_CFLAGS = $(st)

liboscar_la_LDFLAGS = -module -avoid-version

if STATIC_OSCAR

st = -DPURPLE_STATIC_PRPL
noinst_LTLIBRARIES   = liboscar.la
liboscar_la_SOURCES = $(OSCARSOURCES)
liboscar_la_CFLAGS  = $(AM_CFLAGS)

else

st =
pkg_LTLIBRARIES      = liboscar.la
liboscar_la_SOURCES = $(OSCARSOURCES)
liboscar_la_LIBADD  = $(GLIB_LIBS)

endif

AM_CPPFLAGS = \
	-I$(top_srcdir)/libpurple \
	-I$(top_builddir)/libpurple \
	$(GLIB_CFLAGS) \
	$(DEBUG_CFLAGS)
