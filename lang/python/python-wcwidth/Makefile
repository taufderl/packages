# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-wcwidth
PKG_VERSION:=0.9.4
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=wcwidth
PYPI_SOURCE_NAME:=wcwidth
PKG_HASH:=fd8d57d3cdfe570e3265c8fab1885c24e34ef40889c0759c0c304a19e9835954

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-setuptools/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-wcwidth
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Measures the displayed width of unicode strings
  URL:=https://pypi.org/project/wcwidth/
  DEPENDS:= \
	+python3-light
endef

define Package/python3-wcwidth/description
  Measures the displayed width of unicode strings.
endef

$(eval $(call Py3Package,python3-wcwidth))
$(eval $(call BuildPackage,python3-wcwidth))
$(eval $(call BuildPackage,python3-wcwidth-src))
