# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-brotli
PKG_VERSION:=1.1.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=brotli
PYPI_SOURCE_NAME:=Brotli
PKG_HASH:=81de08ac11bcb85841e440c13611c00b67d3bf82698314928d0b676362546724

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-setuptools/host

# the sdist is "Brotli", the wheel it builds is "brotli"
PYTHON3_PKG_WHEEL_NAME:=brotli

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-brotli
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Python bindings for the Brotli compression library
  URL:=https://pypi.org/project/brotli/
  DEPENDS:= \
	+python3-light
endef

define Package/python3-brotli/description
  Python bindings for the Brotli compression library.
endef

$(eval $(call Py3Package,python3-brotli))
$(eval $(call BuildPackage,python3-brotli))
$(eval $(call BuildPackage,python3-brotli-src))
