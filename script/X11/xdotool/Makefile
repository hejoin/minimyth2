GARNAME = xdotool
GARVERSION = 3.20160805.1
CATEGORIES = X11
MASTER_SITES = https://github.com/jordansissel/xdotool/releases/download/v$(GARVERSION)/
DISTFILES = $(DISTNAME).tar.gz
PATCHFILES = set-prefix-to-usr.patch
LICENSE = LGPL2

DESCRIPTION =
define BLURB
endef

DEPENDS   = lang/c xorg/libxkbcommon

BUILD_SCRIPTS   = $(WORKSRC)/Makefile
INSTALL_SCRIPTS = $(WORKSRC)/Makefile

BUILD_ARGS = \
	HOST_CC="$(build_CC)" \
	CROSS_COMPILE="$(compiler_prefix)"

include ../../gar.mk
