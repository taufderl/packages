# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-kaitaistruct
PKG_VERSION:=0.11
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=kaitaistruct
PYPI_SOURCE_NAME:=kaitaistruct
PKG_HASH:=053ee764288e78b8e53acf748e9733268acbd579b8d82a427b1805453625d74b

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-setuptools/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-kaitaistruct
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Kaitai Struct runtime for Python
  URL:=https://pypi.org/project/kaitaistruct/
  DEPENDS:= \
	+python3-light
endef

define Package/python3-kaitaistruct/description
  Kaitai Struct runtime for Python.
endef

$(eval $(call Py3Package,python3-kaitaistruct))
$(eval $(call BuildPackage,python3-kaitaistruct))
$(eval $(call BuildPackage,python3-kaitaistruct-src))
