
GARNAME      = bootfiles-rpi2
GITHASH      = cb2b95d73e9f0b1ebf05e03bb1959603d982feeb
GARVERSION   = 2020-06-14-$(GITHASH)
CATEGORIES   = bootloaders
MASTER_SITES = https://github.com/raspberrypi/firmware/raw/$(GITHASH)/boot/
DISTFILES    = rpi2-boot.scr \
               rpi2-boot.txt \
               bootcode.bin \
               fixup_db.dat \
               fixup.dat \
               fixup_x.dat \
               start_cd.elf \
               start.elf \
               start_x.elf \
               kernel7.img \

export mm_U-BOOT_BOARD_TYPE = rpi_2_defconfig

WORKSRC      = $(WORKDIR)

LICENSE = GPL2

DESCRIPTION =
define BLURB
endef

BUILD_SCRIPTS   = custom
INSTALL_SCRIPTS = custom

include ../../gar.mk

build-custom:
	@$(MAKE) clean -C ../u-boot-rpi
	@$(MAKE) install -C ../u-boot-rpi
	@$(MAKECOOKIE)

install-custom:
	@mkdir -p $(DESTDIR)/boot
	@cp -f $(WORKSRC)/bootcode.bin  $(DESTDIR)/boot/bootcode.bin
	@cp -f $(WORKSRC)/fixup.dat     $(DESTDIR)/boot/fixup.dat
	@cp -f $(WORKSRC)/fixup_db.dat  $(DESTDIR)/boot/fixup_db.dat
	@cp -f $(WORKSRC)/fixup_x.dat   $(DESTDIR)/boot/fixup_x.dat
	@cp -f $(WORKSRC)/rpi2-boot.scr $(DESTDIR)/boot/rpi2-boot.scr
	@cp -f $(WORKSRC)/rpi2-boot.txt $(DESTDIR)/boot/rpi2-boot.txt
	@cp -f $(WORKSRC)/rpi2-boot.scr $(DESTDIR)/boot/boot.scr
	@cp -f $(WORKSRC)/rpi2-boot.txt $(DESTDIR)/boot/boot.txt
	@cp -f $(WORKSRC)/start.elf     $(DESTDIR)/boot/start.elf
	@cp -f $(WORKSRC)/start_cd.elf  $(DESTDIR)/boot/start_cd.elf
	@cp -f $(WORKSRC)/start_x.elf   $(DESTDIR)/boot/start_x.elf
	@cp -f $(DESTDIR)/boot/dtbs/bcm2836-rpi-2-b.dtb $(DESTDIR)/boot/bcm2836-rpi-2-b.dtb
	@# Use this for RPI provided u-boot
	@cp -f $(WORKSRC)/kernel7.img   $(DESTDIR)/boot/kernel7.img
	@# Ust this for mainline u-boot
	@#cp -f $(DESTDIR)$(libdir)/u-boot/rpi2/$(mm_U-BOOT_BOARD_TYPE)/kernel7.img $(DESTDIR)/boot/kernel7.img

clean-all:
	@rm -f $(DESTDIR)/boot/bootcode.bin
	@rm -f $(DESTDIR)/boot/fixup.dat
	@rm -f $(DESTDIR)/boot/fixup_db.dat
	@rm -f $(DESTDIR)/boot/fixup_x.dat
	@rm -f $(DESTDIR)/boot/rpi2-boot.scr
	@rm -f $(DESTDIR)/boot/rpi2-boot.txt
	@rm -f $(DESTDIR)/boot/boot.scr
	@rm -f $(DESTDIR)/boot/boot.txt
	@rm -f $(DESTDIR)/boot/start.elf
	@rm -f $(DESTDIR)/boot/start_cd.elf
	@rm -f $(DESTDIR)/boot/start_x.elf
	@rm -f $(DESTDIR)/boot/kernel7.img
