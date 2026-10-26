# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-pylsqpack
PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=pylsqpack
PYPI_SOURCE_NAME:=pylsqpack
PKG_HASH:=4674adc2c833c1c70a36454f5774e9def94fc3109e4a8464d804af2a2030957a

PKG_LICENSE:=BSD-3-Clause

PKG_BUILD_DEPENDS:=python-setuptools/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-pylsqpack
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Python bindings for ls-qpack (HTTP/3 QPACK)
  URL:=https://pypi.org/project/pylsqpack/
  DEPENDS:= \
	+python3-light
endef

define Package/python3-pylsqpack/description
  Python bindings for ls-qpack (HTTP/3 QPACK).
endef

$(eval $(call Py3Package,python3-pylsqpack))
$(eval $(call BuildPackage,python3-pylsqpack))
$(eval $(call BuildPackage,python3-pylsqpack-src))
