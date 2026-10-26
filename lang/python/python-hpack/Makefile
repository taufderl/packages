# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-hpack
PKG_VERSION:=4.2.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=hpack
PYPI_SOURCE_NAME:=hpack
PKG_HASH:=0895cfa3b5531fc65fe439c05eb65144f123bf7a394fcaa56aa423548d8e45c0

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-setuptools/host python-wheel/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-hpack
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Pure-Python HPACK header encoding (HTTP/2)
  URL:=https://pypi.org/project/hpack/
  DEPENDS:= \
	+python3-light
endef

define Package/python3-hpack/description
  Pure-Python HPACK header encoding (HTTP/2).
endef

$(eval $(call Py3Package,python3-hpack))
$(eval $(call BuildPackage,python3-hpack))
$(eval $(call BuildPackage,python3-hpack-src))
