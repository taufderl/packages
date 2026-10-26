# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-pyparsing
PKG_VERSION:=3.3.3
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=pyparsing
PYPI_SOURCE_NAME:=pyparsing
PKG_HASH:=928ae7e20211f3b6f3915a72f06a0cfd29ab9d24279dd6346b6b1a7146397d36

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-flit-core/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-pyparsing
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Python parsing module
  URL:=https://pypi.org/project/pyparsing/
  DEPENDS:= \
	+python3-light
endef

define Package/python3-pyparsing/description
  Python parsing module.
endef

$(eval $(call Py3Package,python3-pyparsing))
$(eval $(call BuildPackage,python3-pyparsing))
$(eval $(call BuildPackage,python3-pyparsing-src))
