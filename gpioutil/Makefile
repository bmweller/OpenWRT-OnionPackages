#
# Copyright (C) 2015 Onion Corporation
#
# Author: Boken Lin <bl@onion.io>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk
PKG_NAME:=gpioutil
PKG_VERSION:=0.1
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=HEAD
PKG_SOURCE_URL:=https://github.com/OnionIoT/$(PKG_NAME).git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)
PKG_SOURCE:=$(PKG_NAME).tar.gz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)
PKG_BUILD_DEPENDS:=libugpio

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
    SECTION:=utils
    CATEGORY:=Utilities
    SUBMENU:=Onion
    TITLE:=Simple utility to manipulate GPIOs
    DEPENDS:=+libugpio
endef

define Package/$(PKG_NAME)/description
Simple utility to manipulate GPIOs
endef

define Package/$(PKG_NAME)/Build/Compile
	$(MAKE) -C $(PKG_BUILD_DIR) $(PKG_NAME)
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/bin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/$(PKG_NAME) $(1)/bin/$(PKG_NAME)
endef

$(eval $(call BuildPackage,$(PKG_NAME),+libugpio))
