GARNAME = kernel
GARVERSION = $(mm_KERNEL_VERSION)
CATEGORIES = kernel
LICENSE =

DESCRIPTION = 
define BLURB
endef

DEPENDS = \
	kernel/linux-$(mm_KERNEL_VERSION) \
	$(if $(filter armsoc,$(mm_GRAPHICS)),kernel/meson-gx-mali450)

include ../../gar.mk

post-install:
	@rm -rf $(DESTDIR)$(versiondir)/$(GARNAME)
	@rm -rf $(DESTDIR)$(licensedir)/$(GARNAME)

clean-all:
	@$(foreach dir, $(wildcard ../linux-*), $(MAKE) clean     -C $(dir) ; )
	@$(foreach dir, $(wildcard ../linux-*), $(MAKE) clean-all -C $(dir) ; )
	@$(MAKE) clean
	@$(MAKE) clean-all -C ../../kernel-headers/linux-headers
	@$(MAKE) clean-all -C ../../nvidia
	@$(MAKE) clean-all -C ../../bootloaders/bootloader
	@$(MAKE) clean-all -C ../../kernel/meson-gx-mali450
	@$(MAKE) clean     -C ../../kernel-headers/linux-headers
	@$(MAKE) clean     -C ../../nvidia
	@$(MAKE) clean     -C ../../bootloaders/bootloader
	@$(MAKE) clean     -C ../../kernel/meson-gx-mali450
	@$(MAKE) clean     -C ../../system/bbswitch
