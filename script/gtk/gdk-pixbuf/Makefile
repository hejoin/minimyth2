GARNAME = gdk-pixbuf
GARVERSION = 2.30.8
CATEGORIES = gtk
MASTER_SITES = http://ftp.gnome.org/pub/GNOME/sources/gdk-pixbuf/2.30/
DISTFILES = $(DISTNAME).tar.xz
LICENSE = LGPL2

DESCRIPTION =
define BLURB
endef

DEPENDS    = lang/c lang/cxx gtk/glib lib/libjpeg lib/libpng lib/libtiff xorg/xorg
BUILDDEPS  = gtk/gtk-doc

CONFIGURE_SCRIPTS  = $(WORKSRC)/configure
BUILD_SCRIPTS      = $(WORKSRC)/Makefile
INSTALL_SCRIPTS    = $(WORKSRC)/Makefile
ifeq ($(DESTIMG),build)
INSTALL_SCRIPTS   += loaders.cache
endif

CONFIGURE_ARGS = $(DIRPATHS) --build=$(GARBUILD) --host=$(GARHOST) \
	--disable-silent-rules \
	--disable-static \
	--enable-shared \
	--enable-debug=minimal \
	--enable-rebuilds \
	--enable-explicit-deps=auto \
	--enable-nls \
	--disable-rpath \
	--disable-glibtest \
	--disable-modules \
	--with-included-loaders=yes \
	--disable-introspection \
	--disable-gtk-doc \
	--disable-man \
	--enable-Bsymbolic \
	--disable-installed-tests \
	--disable-always-build-tests \
	--disable-coverage \
	--with-gnu-ld \
	--with-libpng \
 	--with-libjpeg \
	--with-libtiff \
	--without-libjasper \
	--with-x11

CONFIGURE_ENV  =
ifneq ($(DESTIMG),build)
CONFIGURE_ENV += \
	gio_can_sniff='yes'
endif

include ../../gar.mk

pre-configure:
	@$(call FIX_LIBTOOL,$(WORKSRC),configure)
	@$(MAKECOOKIE)

install-loaders.cache:
	@$(DESTDIR)$(bindir)/gdk-pixbuf-query-loaders --update-cache
	@$(MAKECOOKIE)

post-install:
	@rm -rf $(DESTDIR)$(libdir)/gdk-pixbuf-2.0/2.10.0/loaders/*.la
	@rm -rf $(DESTDIR)$(libdir)/libgdk_pixbuf-2.0.la
	@rm -rf $(DESTDIR)$(libdir)/libgdk_pixbuf_xlib-2.0.la
	@$(MAKECOOKIE)
