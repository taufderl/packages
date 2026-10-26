# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-aioquic
PKG_VERSION:=1.2.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=aioquic
PYPI_SOURCE_NAME:=aioquic
PKG_HASH:=f91263bb3f71948c5c8915b4d50ee370004f20a416f67fab3dcc90556c7e7199

PKG_LICENSE:=BSD-3-Clause

PKG_BUILD_DEPENDS:=python-setuptools/host python-wheel/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-aioquic
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=QUIC and HTTP/3 implementation in Python
  URL:=https://pypi.org/project/aioquic/
  DEPENDS:= \
	+python3-light \
	+python3-certifi \
	+python3-cryptography \
	+python3-pylsqpack \
	+python3-pyopenssl \
	+python3-service-identity \
	+libopenssl
endef

define Package/python3-aioquic/description
  QUIC and HTTP/3 implementation in Python.
endef

$(eval $(call Py3Package,python3-aioquic))
$(eval $(call BuildPackage,python3-aioquic))
$(eval $(call BuildPackage,python3-aioquic-src))
