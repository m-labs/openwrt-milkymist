#
# Copyright (C) 2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/image.mk

define Image/BuildKernel
	$(CP) $(LINUX_DIR)/arch/lm32/boot/simpleImage.milkymist_one $(BIN_DIR)/
	$(call Image/Build/Initramfs)
endef

define Image/Build
	$(CP) $(KDIR)/root.$(1) $(BIN_DIR)/$(IMG_PREFIX)-root.$(1)
endef

$(eval $(call BuildImage))
