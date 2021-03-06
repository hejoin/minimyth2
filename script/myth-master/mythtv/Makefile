GARNAME = mythtv
GARVERSION = $(MYTHTV_VERSION)
CATEGORIES = $(CATEGORY)
MASTER_SITES = svn://svn.mythtv.org/svn/trunk/
DISTFILES = $(DISTNAME).tar.bz2
PATCHFILES  =

PATCHFILES += 0000-mythprotoserver-add-option-to-ignore-proto-DB-version-checks.patch
PATCHFILES += 0000-configure-set-to-GAR-perl-python.patch.gar

# change to ifeq (0,1) if you want to disable all patches
ifeq (1,1)

# Backend misc patches
PATCHFILES += 0001-Recorders-Delay-to-avoid-no-concurent-recordings-start.patch
PATCHFILES += 0002-Systemstatus-Show-devicename-instead-videodevice.patch
PATCHFILES += 0003-SCR-keep-disecq-always-18V.patch
PATCHFILES += 0004-EIT-make-EIT-start-at-time.patch
PATCHFILES += 0005-EIT-ticket9480-fix-PL-eit-encodings.patch
PATCHFILES += 0006-Mythlink-pretty-with-recgroup-subdir.patch
PATCHFILES += 0007-TMDB-pull103-Add-heuristic-in-TMDB-script-to-detect-movie-release-years.patch
PATCHFILES += 0009-disable-python-warnings-because-py2.6.patch
# Adds metadata grabbers timeout be configurable
PATCHFILES += 0011-Metadata-allow-graber-timeout-configurable.patch
# Fixes issue with only 3 menu entries in MythMediaStream theme. t.b.i why?
PATCHFILES += 0013-revert-42bae47-MythMainWindow-Norm-With-very-small-values-of-x-scal.patch

# Comflagging related patches
PATCHFILES += 0016-Mythcommflag-ticket13335-add-3-settings-to-enhance-logo-detection.patch

# UPnP patches
PATCHFILES += 0030-UPnP-Change-reported-ver-to-1.patch
PATCHFILES += 0031-UPnP-Reduce-startup-latency-by-moving-blocking-code-to-own-thread.patch
PATCHFILES += 0032-UPnP-Add-playlist-recently-added-played-entries-to-upnp-music.patch

# Some patches for better logging
PATCHFILES += 0050-Loging-Add-better-EIT-verbosity.patch
PATCHFILES += 0051-Loging-Add-better-TID-verbosity.patch
PATCHFILES += 0052-Loging-Decrease-some-PMT-DVB-errors-Loging.patch
PATCHFILES += 0053-Loging-Add-verbose-dvb-lock-loging.patch
PATCHFILES += 0054-Loging-Add-better-loging-for-failed-tunings.patch
PATCHFILES += 0055-Loging-Add-AFD-original-channels-to-audio-format-loging.patch
PATCHFILES += 0056-Loging-Add-signal-monitor-warning-msg-if-NID-or-TSID-dont-match.patch
PATCHFILES += 0057-Loging-Mythmusic-log-the-shoutcast-metadata-and-format.patch
PATCHFILES += 0058-Loging-add-some-DB-GetSetting-logging.patch

# Minimyth related patches
PATCHFILES += 0100-Minimyth-Add-maintain-menu.patch
PATCHFILES += 0101-Minimyth-Add-disable-optical-disc-in-menu.patch
PATCHFILES += 0102-Minimyth-Add-phone-entry-in-menu.patch
PATCHFILES += 0103-Minimyth-Add-optical-rip-to-menu.patch
PATCHFILES += 0104-Minimyth-Add-netflix-to-menus.patch
#PATCHFILES += 0105-Minimyth-defaults.patch
PATCHFILES += 0106-hack-for-correct-perl-bindings-install.patch
PATCHFILES += 0107-settings-make-language-setting-per-host-setting.patch
PATCHFILES += 0108-audio-revert-91e5b1b4-fix-audio-noise-on-some-platofrms.patch
PATCHFILES += 0109-install-fix-nv-codec-headers-loc.patch

# v4l2-request support in ffmpeg
# https://github.com/Kwiboo/FFmpeg/commits/v4l2-request-hwaccel-master
PATCHFILES += 0151-ffmpeg-v4l2request-avutil-add-av_buffer_pool_flush.patch
PATCHFILES += 0152-ffmpeg-v4l2request-Add-common-V4L2-request-API-code.patch
PATCHFILES += 0153-ffmpeg-v4l2request-Add-V4L2-request-API-mpeg2-hwaccel.patch
PATCHFILES += 0154-ffmpeg-v4l2request-Add-V4L2-request-API-h264-hwaccel.patch
PATCHFILES += 0155-ffmpeg-v4l2request-Add-V4L2-request-API-hevc-hwaccel.patch
PATCHFILES += 0156-ffmpeg-v4l2request-Add-V4L2-request-API-vp8-hwaccel.patch
PATCHFILES += 0157-ffmpeg-v4l2request-Add-and-use-private-linux-headers-for-V4L2-request-A.patch
PATCHFILES += 0158-ffmpeg-v4l2request-hwcontext_drm-do-not-require-drm-device.patch
PATCHFILES += 0159-ffmpeg-v4l2request-avcodec-h264-parse-idr_pic_id.patch
PATCHFILES += 0160-ffmpeg-v4l2request-avcodec-h264-parse-ref_pic_marking_size_in_bits-and-.patch
PATCHFILES += 0161-ffmpeg-v4l2request-HACK-add-dpb-flags-for-reference-usage-and-field-pic.patch
PATCHFILES += 0162-ffmpeg-v4l2request-WIP-v4l2-request-rolling-timestamps.patch
PATCHFILES += 0163-ffmpeg-v4l2request-hevc-Set-SPS-control-at-initialization.patch
PATCHFILES += 0163-configure-add-v4l2request-support.patch
# backports v4l2 related from ffmpeg master
# https://github.com/FFmpeg/FFmpeg/commit/8a8966295fbc9278042f4be76b795fea39f9a810
PATCHFILES += 0164-ffmpeg-avcodec-v4l2_context-Use-AVERROR-macro.patch
# https://github.com/tmm1/FFmpeg/commit/a0a00b958c524f3b0e2ca26d60dad1a674f872c7
PATCHFILES += 0165-ffmpeg-avcodec-v4l2m2m-clean-up-buffer-options-and-pick-sane-defaults.patch
# https://github.com/tmm1/FFmpeg/commit/3e397f382974cca43e3fbb24bb850fc3f3225c30
PATCHFILES += 0166-ffmpeg-avcodec-v4l2_m2m_dec-remove-temporary-avpkt-and-read-directyl-to-buffer.patch
# https://github.com/tmm1/FFmpeg/commit/196bab90a29323722050111e936532ac9ac9bfda
PATCHFILES += 0167-ffmpeg-avcodec-handle-errors-more-explicitly.patch
# https://github.com/FFmpeg/FFmpeg/commit/6ee7375ef50b6744c33d988c0ea2fb1780a838f0
PATCHFILES += 0168-avcodec-v4l2_m2m-Avoid-using-intermediate-buffer.patch
# https://github.com/FFmpeg/FFmpeg/commit/b761ae072a169eb183abe0785a258b9787e267d3
PATCHFILES += 0169-ffmpeg-libavdevice-produce-0byte-if-dequeued-size-unexpected.patch
# Add some v4l2 logging
PATCHFILES += 0170-ffmpeg-libavcodec-log-requested-pixfmt.patch
# required for AML HD playbck in MythTV
PATCHFILES += 0171-v4l2decoder-increase-cap-buffers-to-16.patch
# use improvements from KODI
PATCHFILES += 0172-ffmpeg-sync-v4l2_m2m-to-kodi9.2.patch
# backports v4l2 related from ffmpeg master
# https://github.com/FFmpeg/FFmpeg/commit/8ac8e905e934aaae3f3ad3a0e2f2066b55b1c560
PATCHFILES += 0173-ffmpeg-avcodec-v4l2_m2m-handle-v4l2-end-of-stream-event.patch
# https://github.com/FFmpeg/FFmpeg/commit/e3b49aaa4eed7955e243b110e1209960ba5aaf74
PATCHFILES += 0176-ffmpeg-avcodec-v4l2_context-Drop-empty-packet-while-draining.patch
# https://github.com/FFmpeg/FFmpeg/commit/c76b2bf0b4e752455e5ffbd7dee12e935c2eaccd
PATCHFILES += 0177-ffmpeg-avcodec-v4l2_context-Finish-draining-if-V4L2_BUF_FLAG_LAST-is-set.patch
# https://github.com/FFmpeg/FFmpeg/commit/2a9d62356152d4ef079416101664f26d2562c681
PATCHFILES += 0178-ffmpeg-avcodec-v4l2_context-Log-warning-when-all-capture-buffs-in-userspace.patch
# lrusak seeking fix on v4l2_m2m decoders (not working on rpi/amlogic)
# https://github.com/lrusak/FFmpeg/commit/a28eba7a06e70d2ee204fb4a6f6abe61a729edd2
# PATCHFILES += 0179-ffmpeg-libavcodec-v4l2m2m-implement-flush.patch
# Debuging v4l2 vdec polling in ffmpeg
# PATCHFILES += 0180-ffmpeg-libavcodec-log-v4l2-decoder-poll.patch
# Mediamonitor patches
PATCHFILES += 0200-Mediamonitor-Exclude-minimyth-from-mediamonitor-paths.patch
PATCHFILES += 0201-Mediamonitor-reduce-udisks-timeout-to-1500msec.patch
PATCHFILES += 0202-Mediamonitor-make-mediamonitor-bluray-mounts-persistent.patch
# Fixes issue with LiveTV 'All tuners busy' just after FE resume (if media monitor is not enabled)
PATCHFILES += 0203-Mediamonitor-revert-16086d2-Honor-the-MonitorDrives-setting.patch
# Added UI to select multimedia handler in multimode CD's
PATCHFILES += 0204-Mediamonitor-add-UI-to-select-preferred-media-handler.patch

# Misc frontend patches
PATCHFILES += 0211-decrease-minQt-ver-to-4.8.patch
PATCHFILES += 0212-external-udfread-fix-arm5te-compilation.patch
PATCHFILES += 0213-MythDVD-Fix-broken-DVDmenu.patch

# Patches related to OSD
PATCHFILES += 0221-OSD-fix-_LMSC-on-osd.patch
PATCHFILES += 0222-OSD-ticket9633-progressbar-on-osd.patch
PATCHFILES += 0223-OSD-Add-mythnotification-custom-styles-support-via-UDP.patch
PATCHFILES += 0224-OSD-Add-status-notify-to-mythmediacenter-wide.patch
PATCHFILES += 0225-OSD-Add-status-notify-to-mythmediacenter.patch
#PATCHFILES += 0227-OSD-Add-interlaced-status-to-OSD-debug-screen.patch

# Patches enhancing Network Control
PATCHFILES += 0283-NetworkControl-Add-set-query-loglevel-commands.patch

# Nice Roger Siddons guide grid enhacement
PATCHFILES += 0304-ticket12683-MythUI-Implement-zoomable-GuideGrids-v2.patch

# Roger Siddons patches from PeterBennet repo
PATCHFILES += 0305-ticket12809-Enable-Play-from-last-play-position.patch
PATCHFILES += 0307-ticket12809-Playback-Watchlist-Improvements.patch
PATCHFILES += 0308-ticket12809-Playback-Add-Unfinished-recording-filter.patch


# --------Patches 400+ are plugins patches---------------------

# Various mythmusic patches
PATCHFILES += 0400-Mythmusic-ticket10710-play-tracks-from-edit.patch
PATCHFILES += 0401-MythMusic-disable-screensaver-only-in-fullscreen.patch
PATCHFILES += 0404-MythMusic-Prevent-corruption-of-ripped-CD-music-file.patch
PATCHFILES += 0405-MythMusic-Wait-for-scanner-and-eject-threads-before-deleting.patch
PATCHFILES += 0406-MythMusic-Make-initial-scan-by-CD-ripper-run-in-background.patch

# Various mythweather patches
PATCHFILES += 0450-MythWeather-Prevent-log-error-report-when-widget-not-found.patch

endif

LICENSE = GPL2

DESCRIPTION = 
define BLURB
endef

DEPENDS = \
	lang/cxx \
	db/mysql \
	db/sqlite \
	lib/alsa-lib \
	lib/avahi \
	lib/exiv2 \
	lib/fftw3 \
	lib/freetype \
	lib/lame \
	lib/libass \
	lib/libavc1394 \
	lib/libcdio \
	lib/libcdio-paranoia \
	lib/libiec61883 \
	lib/libxml2 \
	lib/openssl \
	lib/libsamplerate \
	lib/libbluray \
	lib/SDL2 \
	lib/taglib \
	lib/lzo \
	devel/zlib \
	devel/yasm \
	python/python \
	python/python-future \
	python/python-lxml \
	python/python-MySQL-python \
	python/python-requests-cache \
	python/python-simplejson \
	python/python-urlgrabber \
	perl/perl-DBD-mysql \
	perl/perl-DBI \
	perl/perl-HTTP-Message \
	perl/perl-IO-Socket-INET6 \
	perl/perl-libwww-perl \
	perl/perl-Net-UPnP \
	perl/perl-XML-Simple \
	system/lirc \
	system/eudev \
	X11/libvdpau \
	X11/libva \
	xorg/xorg \
	qt/qt5 \
	qt/qt5-webkit \

BUILDDEPS = \
	python/python \
	python/python-future \
	python/python-lxml \
	python/python-MySQL-python \
	python/python-requests-cache \
	python/python-simplejson \
	python/python-urlgrabber \
	perl/perl-DBD-mysql \
	perl/perl-DBI \
	perl/perl-HTTP-Message \
	perl/perl-IO-Socket-INET6 \
	perl/perl-libwww-perl \
	perl/perl-Net-UPnP \
	perl/perl-XML-Simple \

DISTNAME_SHORT = $(GARNAME)-$(MYTHTV_GARVERSION_SHORT)

CATEGORY := $(shell basename $(shell dirname $(shell pwd)))

PWD := $(shell pwd)

CONFIGURE_SCRIPTS = $(WORKSRC)/mythtv/configure
BUILD_SCRIPTS     = $(WORKSRC)/mythtv/Makefile
INSTALL_SCRIPTS   = $(WORKSRC)/mythtv/Makefile source


CONFIGURE_ARGS = \
	--compile-type=$(if $(filter yes,$(mm_DEBUG)),"debug","release") \
	--prefix="$(DESTDIR)$(prefix)" \
	--runprefix="$(prefix)" \
	--libdir-name="$(patsubst $(prefix)/%,%,$(libdir))" \
	--disable-ccache \
	--disable-distcc \
	--bindir="$(DESTDIR)$(bindir)" \
	--datadir="$(DESTDIR)$(datadir)/mythtv" \
	--libdir="$(DESTDIR)$(libdir)" \
	--incdir="$(DESTDIR)$(includedir)/mythtv" \
	--shlibdir="$(DESTDIR)$(libdir)" \
	--mandir="$(DESTDIR)$(mandir)" \
	$(if $(filter -Os,$(CFLAGS)),--enable-small) \
	--cross-prefix="$(compiler_prefix)" \
	--enable-cross-compile \
	--sysroot="$(DESTDIR)$(rootdir)" \
	--sysinclude="$(DESTDIR)$(includedir)" \
	--target-os="linux" \
	--nm="$(NM)" \
	--as="$(CC)" \
	--cc="$(CC)" \
	--cxx="$(CXX)" \
	--ld="$(CC)" \
	--qmake="$(DESTDIR)$(qt5bindir)/qmake" \
	--host-cc="$(build_CC)" \
	--host-cflags="$(build_CFLAGS)" \
	--host-ldflags="$(build_LDFLAGS)" \
	--extra-cflags="$(CFLAGS)" \
	--extra-cxxflags="$(CXXFLAGS)" \
	--extra-ldflags="$(LDFLAGS)" \
	--enable-symbol-visibility \
	--arch=$(GARCH_FAMILY) \
	--disable-altivec \
	--enable-amd3dnow \
	--enable-amd3dnowext \
	--enable-mmx \
	--enable-sse \
	--enable-ssse3 \
	--enable-yasm \
	--disable-proc-opt \
	--enable-audio-oss \
	--enable-audio-alsa \
	--disable-audio-jack \
	--disable-audio-pulseoutput \
	--disable-valgrind \
	--enable-lirc \
	--disable-joystick-menu \
	--enable-firewire \
	--disable-hdhomerun \
	--disable-ceton \
	--enable-v4l2 \
	--enable-vaapi \
	--enable-ivtv \
	--enable-hdpvr \
	--enable-dvb \
	--dvb-path="$(DESTDIR)$(includedir)" \
	--disable-asi \
	--enable-x11 \
	--x11-path="$(DESTDIR)$(includedir)" \
	--enable-xrandr \
	--disable-dxva2 \
	$(if $(filter arm arm64,$(GARCH_FAMILY)), \
		--disable-vdpau) \
	--disable-mac-bundle \
	--enable-libxml2 \
	--enable-libdns_sd \
	--enable-libcrypto \
	--without-bindings="php" \
	--with-bindings="perl" \
	--with-bindings="python" \
	--enable-pic \
	--disable-libcec \
	--pkg-config="$(build_DESTDIR)$(build_bindir)/pkg-config" \
	--enable-ffplay \
	--enable-sdl2 \
	--python="python" \

CONFIGURE_ENV  = $(MYTHTV_CONFIGURE_ENV)
BUILD_ENV      = $(MYTHTV_BUILD_ENV)
INSTALL_ENV    = $(MYTHTV_INSTALL_ENV)

BUILD_ENV     += PYTHONXCPREFIX=$(DESTDIR)$(prefix)
INSTALL_ENV   += PYTHONPATH=$(DESTDIR)$(PYTHON_libdir)/site-packages

GAR_EXTRA_CONF += python/python/package-api.mk
include ../../gar.mk

ifneq (,$(findstring rpi,$(mm_KERNEL_VERSION)))
CONFIGURE_ARGS += --disable-v4l2request
else
CONFIGURE_ARGS += --enable-v4l2request
endif

CPPFLAGS += -I$(DESTDIR)$(includedir)/avahi-compat-libdns_sd
CFLAGS   += -I$(DESTDIR)$(includedir)/avahi-compat-libdns_sd
CXXFLAGS += -I$(DESTDIR)$(includedir)/avahi-compat-libdns_sd

CPPFLAGS += -fPIC
CFLAGS   += -fPIC

ifeq ($(mm_DEBUG),yes)
CFLAGS   := $(filter-out -O%, $(CFLAGS)) -O0
CXXFLAGS := $(filter-out -O%, $(CXXFLAGS)) -O0
endif

# mythtv don't compiles with gcc5.3.0 LTO
CFLAGS   := $(filter-out -flto, $(CFLAGS))
CXXFLAGS := $(filter-out -flto, $(CXXFLAGS))
LDFLAGS  := $(filter-out -flto, $(LDFLAGS))

svn//%/$(DISTNAME).tar.bz2:
	@$(call FETCH_SVN, http://$*, $(MYTHTV_SVN_VERSION), $(DISTNAME))
	@$(MAKECOOKIE)

checksum-$(DISTNAME).tar.bz2:
	@$(MAKECOOKIE)

install-source:
	@rm -rf $(DESTDIR)$(MYTHTV_SOURCEDIR)
	@mkdir -p $(DESTDIR)$(MYTHTV_SOURCEDIR)
	@rm -rf $(DESTDIR)$(MYTHTV_SOURCEDIR)
	@ln -sf $(PWD)/$(WORKSRC)/mythtv $(DESTDIR)$(MYTHTV_SOURCEDIR)
	@$(MAKECOOKIE)

post-install: post-install-mythtv-version
	@rm -f $(DESTDIR)$(bindir)/mythtv
	@mv $(DESTDIR)$(bindir)/mythavtest $(DESTDIR)$(bindir)/mythtv
	@$(MAKECOOKIE)

pre-configure:
	@#Myth ver.containing also MM2 version
	@#sed -i -e "s/MYTH_SOURCE_VERSION.*/MYTH_SOURCE_VERSION \"$(MYTHTV_GIT_VERSION)-v`grep "^mm_VERSION_MINIMYTH" ~/.minimyth/minimyth.conf.mk | sed -e 's/.*\?=\s*\(.*\)/\1/'`\"/" $(WORKSRC)/mythtv/version.sh
	@sed -i -e "s/MYTH_SOURCE_VERSION.*/MYTH_SOURCE_VERSION \"$(MYTHTV_GIT_VERSION)\"/" $(WORKSRC)/mythtv/version.sh
	@sed -i -e "s/MYTH_SOURCE_PATH.*/MYTH_SOURCE_PATH \"$(mm_MYTH_VERSION)\"/" $(WORKSRC)/mythtv/version.sh
	@$(MAKECOOKIE)

clean-all:
	@rm -rf $(DESTDIR)$(bindir)/mtd
	@rm -rf $(DESTDIR)$(bindir)/myth*
	@rm -rf $(DESTDIR)$(datadir)/myth*
	@rm -rf $(DESTDIR)$(includedir)/myth*
	@rm -rf $(DESTDIR)$(libdir)/libmyth*
	@rm -rf $(DESTDIR)$(libdir)/myth*
	@rm -rf $(DESTDIR)$(libdir)/python*/site-packages/MythTV
	@rm -rf $(DESTDIR)$(libdir)/python*/site-packages/MythTV-*
	@$(foreach dir,$(filter-out %/Makefile,$(wildcard ../../myth/* ../../myth-*/*)),$(MAKE) -C $(dir) clean ; )

source-update:
	@$(MAKE) source-update-source
	@$(MAKE) source-update-patches

source-update-source:
	@$(MAKE) clean
	@$(MAKE) fetch
	@$(MAKE) $(GARCHIVEDIR)/$(DISTNAME).tar.bz2
	@$(MAKE) clean

source-update-patches:
	@$(MAKE) clean
	@$(MAKE) extract
	@$(foreach PATCHFILE, $(PATCHFILES), \
		cd $(WORKDIR) || exit 1 ; \
		mv $(DISTNAME) $(DISTNAME)-old || exit 1 ; \
		cp -r $(DISTNAME)-old $(DISTNAME)-new || exit 1 ; \
		cd $(DISTNAME)-new || exit 1 ; \
		SIMPLE_BACKUP_SUFFIX=.gar-source-update-patches patch -p1 < ../../../files/$(PATCHFILE) || exit 1 ; \
		cd ../ || exit 1 ; \
		find $(DISTNAME)-new -name *.gar-source-update-patches -exec rm {} \; || exit 1 ; \
		( diff -Naur $(DISTNAME)-old $(DISTNAME)-new > ../../files/$(PATCHFILE) ; test $$? -lt 2 ) || exit 1 ; \
		rm -fr $(DISTNAME)-old || exit 1 ; \
		mv $(DISTNAME)-new $(DISTNAME) || exit 1 ; \
		cd ../../ || exit 1 ; \
		rm -f checksums~ || exit 1 ; \
		cat checksums | grep -v $(DOWNLOADDIR)/$(PATCHFILE) > checksums~ || true ; \
		md5sum $(DOWNLOADDIR)/$(PATCHFILE) >> checksums~ || exit 1 ; \
		rm -f checksums || exit 1 ; \
		mv -f checksums~ checksums || exit 1 ; )
	@$(MAKE) clean
