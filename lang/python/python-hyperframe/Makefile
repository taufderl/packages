# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-hyperframe
PKG_VERSION:=6.1.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=hyperframe
PYPI_SOURCE_NAME:=hyperframe
PKG_HASH:=f630908a00854a7adeabd6382b43923a4c4cd4b821fcb527e6ab9e15382a3b08

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-setuptools/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-hyperframe
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Pure-Python HTTP/2 framing
  URL:=https://pypi.org/project/hyperframe/
  DEPENDS:= \
	+python3-light
endef

define Package/python3-hyperframe/description
  Pure-Python HTTP/2 framing.
endef

$(eval $(call Py3Package,python3-hyperframe))
$(eval $(call BuildPackage,python3-hyperframe))
$(eval $(call BuildPackage,python3-hyperframe-src))
