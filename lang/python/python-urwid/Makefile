# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-urwid
PKG_VERSION:=4.0.13
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=urwid
PYPI_SOURCE_NAME:=urwid
PKG_HASH:=23afb15197b9e3b656b8c55bb3e18d50463c34db1982ec81ef5034525bea6c76

PKG_LICENSE:=LGPL-2.1-or-later

PKG_BUILD_DEPENDS:=python-setuptools/host python-setuptools-scm/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-urwid
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Console user interface library
  URL:=https://pypi.org/project/urwid/
  DEPENDS:= \
	+python3-light \
	+python3-wcwidth \
	+python3-typing-extensions
endef

define Package/python3-urwid/description
  Console user interface library.
endef

$(eval $(call Py3Package,python3-urwid))
$(eval $(call BuildPackage,python3-urwid))
$(eval $(call BuildPackage,python3-urwid-src))
