# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-publicsuffix2
PKG_VERSION:=2.20191221
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=publicsuffix2
PYPI_SOURCE_NAME:=publicsuffix2
PKG_HASH:=00f8cc31aa8d0d5592a5ced19cccba7de428ebca985db26ac852d920ddd6fe7b

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-setuptools/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-publicsuffix2
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Public Suffix List with a bundled list
  URL:=https://pypi.org/project/publicsuffix2/
  DEPENDS:= \
	+python3-light
endef

define Package/python3-publicsuffix2/description
  Public Suffix List with a bundled list.
endef

$(eval $(call Py3Package,python3-publicsuffix2))
$(eval $(call BuildPackage,python3-publicsuffix2))
$(eval $(call BuildPackage,python3-publicsuffix2-src))
