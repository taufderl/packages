# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-h2
PKG_VERSION:=4.4.1
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=h2
PYPI_SOURCE_NAME:=h2
PKG_HASH:=4e866ffb1a869ae14dd9b5e6beb5c24a13da0495ad72b65925ded182521c1516

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-setuptools/host python-wheel/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-h2
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Pure-Python HTTP/2 protocol stack
  URL:=https://pypi.org/project/h2/
  DEPENDS:= \
	+python3-light \
	+python3-hpack \
	+python3-hyperframe
endef

define Package/python3-h2/description
  Pure-Python HTTP/2 protocol stack.
endef

$(eval $(call Py3Package,python3-h2))
$(eval $(call BuildPackage,python3-h2))
$(eval $(call BuildPackage,python3-h2-src))
