#
# Copyright (C) 2009 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

ARCH:=lm32
BOARD:=lm32
BOARDNAME:=Milkymist
FEATURES:=usb nommu binfmt_flat ext4

LINUX_VERSION:=3.0

DEVICE_TYPE:=vj-station

include $(INCLUDE_DIR)/target.mk

KERNELNAME:="simpleImage.milkymist_one"
DEFAULT_PACKAGES:=base-files libc libgcc busybox dropbear mtd

$(eval $(call BuildTarget))
