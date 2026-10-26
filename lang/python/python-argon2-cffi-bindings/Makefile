# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-argon2-cffi-bindings
PKG_VERSION:=25.1.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=argon2-cffi-bindings
PYPI_SOURCE_NAME:=argon2_cffi_bindings
PKG_HASH:=b957f3e6ea4d55d820e40ff76f450952807013d361a65d7f28acc0acbf29229d

PKG_LICENSE:=MIT

PKG_BUILD_DEPENDS:=python-setuptools/host python-setuptools-scm/host python-cffi/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

# setup.py checks the build host's CPU and would pass -msse2 to the target compiler
PYTHON3_PKG_BUILD_VARS += ARGON2_CFFI_USE_SSE2=0

define Package/python3-argon2-cffi-bindings
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Low-level CFFI bindings for Argon2
  URL:=https://pypi.org/project/argon2-cffi-bindings/
  DEPENDS:= \
	+python3-light \
	+python3-cffi
endef

define Package/python3-argon2-cffi-bindings/description
  Low-level CFFI bindings for Argon2.
endef

$(eval $(call Py3Package,python3-argon2-cffi-bindings))
$(eval $(call BuildPackage,python3-argon2-cffi-bindings))
$(eval $(call BuildPackage,python3-argon2-cffi-bindings-src))
