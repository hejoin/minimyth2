GARNAME      = arm-trusted-firmware-20200310-h6
GARVERSION   = 65012c08922fa5646ca7ca485036dfd901cae360
CATEGORIES   = kernel
MASTER_SITES = https://github.com/ARM-software/arm-trusted-firmware/archive/
DISTFILES    = $(GARVERSION).zip
WORKSRC      = $(WORKDIR)/arm-trusted-firmware-$(GARVERSION)

LICENSE = GPL2

DESCRIPTION =
define BLURB
endef

DEPENDS   = lang/c

CONFIGURE_SCRIPTS   = 
BUILD_SCRIPTS       = custom
INSTALL_SCRIPTS     = 

include ../../gar.mk

BUILD_ARGS = \
	CROSS_COMPILE=$(compiler_prefix) \

build-custom:
	@echo "Building bl31 trusted firmware for Allwinner H6..."
	@$(BUILD_ARGS) $(MAKE) -C $(WORKSRC) PLAT=sun50i_h6 DEBUG=1 bl31
	@echo "Instaling bl31 trusted firmware for Allwinner H6..."
	@mkdir -p "$(DESTDIR)$(libdir)/u-boot/h6"
	@cp $(WORKSRC)/build/sun50i_h6/debug/bl31.bin $(DESTDIR)$(libdir)/u-boot/h6/bl31.bin
	@$(MAKECOOKIE)

clean-all:
	@rm -f $(DESTDIR)$(libdir)/u-boot/h6/bl31.bin
