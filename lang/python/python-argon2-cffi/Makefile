# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-argon2-cffi
PKG_VERSION:=25.1.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=argon2-cffi
PYPI_SOURCE_NAME:=argon2_cffi
PKG_HASH:=694ae5cc8a42f4c4e2bf2ca0e64e51e23a040c6a517a85074683d3959e1346c1

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-hatchling/host python-hatch-vcs/host python-hatch-fancy-pypi-readme/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-argon2-cffi
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Argon2 password hashing for Python
  URL:=https://pypi.org/project/argon2-cffi/
  DEPENDS:= \
	+python3-light \
	+python3-argon2-cffi-bindings
endef

define Package/python3-argon2-cffi/description
  Argon2 password hashing for Python.
endef

$(eval $(call Py3Package,python3-argon2-cffi))
$(eval $(call BuildPackage,python3-argon2-cffi))
$(eval $(call BuildPackage,python3-argon2-cffi-src))
