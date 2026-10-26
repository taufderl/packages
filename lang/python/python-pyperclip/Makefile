# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-pyperclip
PKG_VERSION:=1.11.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=pyperclip
PYPI_SOURCE_NAME:=pyperclip
PKG_HASH:=244035963e4428530d9e3a6101a1ef97209c6825edab1567beac148ccc1db1b6

PKG_LICENSE:=BSD-3-Clause

PKG_BUILD_DEPENDS:=python-setuptools/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-pyperclip
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Cross-platform clipboard module
  URL:=https://pypi.org/project/pyperclip/
  DEPENDS:= \
	+python3-light
endef

define Package/python3-pyperclip/description
  Cross-platform clipboard module.
endef

$(eval $(call Py3Package,python3-pyperclip))
$(eval $(call BuildPackage,python3-pyperclip))
$(eval $(call BuildPackage,python3-pyperclip-src))
