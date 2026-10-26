# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-ldap3
PKG_VERSION:=2.9.1
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=ldap3
PYPI_SOURCE_NAME:=ldap3
PKG_HASH:=f3e7fc4718e3f09dda568b57100095e0ce58633bcabbed8667ce3f8fbaa4229f

PKG_LICENSE:=LGPL-3.0-or-later

PKG_BUILD_DEPENDS:=python-setuptools/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-ldap3
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Pure-Python LDAP v3 client
  URL:=https://pypi.org/project/ldap3/
  DEPENDS:= \
	+python3-light \
	+python3-pyasn1
endef

define Package/python3-ldap3/description
  Pure-Python LDAP v3 client.
endef

$(eval $(call Py3Package,python3-ldap3))
$(eval $(call BuildPackage,python3-ldap3))
$(eval $(call BuildPackage,python3-ldap3-src))
