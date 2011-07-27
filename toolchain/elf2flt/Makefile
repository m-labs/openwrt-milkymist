include $(TOPDIR)/rules.mk

PKG_NAME:=elf2flt

PKG_SOURCE_URL:=http://git.serverraum.org/git/mw/elf2flt.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=08d80172231853b2d2a7bf03d94a9d7115c3d348
PKG_VERSION:=$(PKG_SOURCE_VERSION)
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_MD5SUM:=

include $(INCLUDE_DIR)/toolchain-build.mk

BINUTILS_DIR := $(BUILD_DIR_TOOLCHAIN)/binutils

HOST_CONFIGURE_ARGS+= \
	--target=$(REAL_GNU_TARGET_NAME) \
	--with-bfd-include-dir=$(BINUTILS_DIR)/include/ \
	--with-libbfd=$(TOOLCHAIN_DIR)/lib/libbfd.a \
	--with-libiberty=$(TOOLCHAIN_DIR)/lib/libiberty.a \
	--disable-emit-relocs --enable-always-reloc-text

HOST_CFLAGS+=-I$(BINUTILS_DIR)/bfd

$(eval $(call HostBuild))
