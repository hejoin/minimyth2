GARNAME = glu
GARVERSION = 9.0.0-20160610-0bf42e4
CATEGORIES = $(CATEGORY)
MASTER_SITES  = git://anongit.freedesktop.org/git/mesa/$(GARNAME)/
DISTFILES = $(DISTNAME).tar.bz2
PATCHFILES = fix-missing-stddef.h.patch
LICENSE =

DESCRIPTION = 
define BLURB
endef

DEPENDS = lang/c lang/cxx \
	$(if $(filter mesa,$(mm_OPENGL_PROVIDER)),$(CATEGORY)/mesa) \
	$(if $(filter lima,$(mm_OPENGL_PROVIDER)),$(CATEGORY)/mesa-lima) \

CATEGORY := $(shell basename $(shell dirname $(shell pwd)))

CONFIGURE_SCRIPTS  = $(WORKSRC)/configure
BUILD_SCRIPTS      = $(WORKSRC)/Makefile
INSTALL_SCRIPTS    = $(WORKSRC)/Makefile

CONFIGURE_ARGS = $(DIRPATHS) --build=$(GARBUILD) --host=$(GARHOST) \
	--disable-silent-rules \
	--disable-debug \
	--disable-osmesa \
	--disable-static \
	--with-gnu-ld

include ../../gar.mk

git//%$(DISTNAME).tar.bz2:
	@$(call FETCH_GIT, $*, $(word 3,$(subst -, ,$(GARVERSION))), $(DISTNAME))
	@$(MAKECOOKIE)

checksum-$(DISTNAME).tar.bz2:
	@$(MAKECOOKIE) 

pre-configure:
	@$(call RUN_AUTOTOOLS)
	@$(MAKECOOKIE)

post-install:
	@rm -f $(DESTDIR)$(libdir)/libGLU.la
	@$(MAKECOOKIE)
