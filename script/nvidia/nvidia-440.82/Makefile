NVIDIA_MAJOR_VERSION = 440
NVIDIA_MINOR_VERSION = 82
NVIDIA_TEENY_VERSION =
PATCHFILES           = nvidia-440.82-fix-5.7-kernel-compile.patch

BUILD_SCRIPTS   = nvidia
INSTALL_SCRIPTS = nvidia

BUILD_ARGS = $(NVIDIA_MAKE_ARGS)
BUILD_ENV  = $(NVIDIA_MAKE_ENV)

export IGNORE_MISSING_MODULE_SYMVERS=1

GAR_EXTRA_CONF += kernel/linux-$(mm_KERNEL_VERSION)/package-api.mk nvidia/nvidia/package-api.mk
include ../../gar.mk

post-install:
	@cd files; ./generate-nvidia-udev-rule.sh $(NVIDIA_MAJOR_VERSION).$(NVIDIA_MINOR_VERSION)
	@$(MAKECOOKIE)
