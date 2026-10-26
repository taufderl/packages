# SPDX-License-Identifier: GPL-2.0-only
#
# mitmproxy is installed from its pure-Python wheel: PyPI has no sdist, and the
# GitHub sources lack the prebuilt mitmweb web interface.

include $(TOPDIR)/rules.mk

PKG_NAME:=mitmproxy
PKG_VERSION:=12.3.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-py3-none-any.whl
PKG_SOURCE_URL:=https://files.pythonhosted.org/packages/e8/aa/a1ef423def5e405455cca69e938b0961c36091f5ac69bc4d15809b93df29/
PKG_HASH:=29fd9e934bad86a321ff345ec141f894dbcc1ec9e3bf5deffba9ac2ea9db3c61

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

include $(INCLUDE_DIR)/package.mk
include ../../lang/python/python3-version.mk

PYTHON3_PKG_DIR:=/usr/lib/python$(PYTHON3_VERSION)/site-packages

define Package/mitmproxy
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Interactive TLS-capable intercepting HTTP proxy
  URL:=https://mitmproxy.org/
  DEPENDS:= \
	+python3 \
	+python3-aioquic \
	+python3-argon2-cffi \
	+python3-asgiref \
	+python3-bcrypt \
	+python3-brotli \
	+python3-certifi \
	+python3-cryptography \
	+python3-flask \
	+python3-h11 \
	+python3-h2 \
	+python3-hyperframe \
	+python3-kaitaistruct \
	+python3-ldap3 \
	+python3-mitmproxy-rs \
	+python3-pyopenssl \
	+python3-pyparsing \
	+python3-pyperclip \
	+python3-publicsuffix2 \
	+python3-ruamel-yaml \
	+python3-sortedcontainers \
	+python3-tornado \
	+python3-urwid \
	+python3-wsproto
endef

define Package/mitmproxy/description
  mitmproxy is an interactive, TLS-capable intercepting proxy for HTTP/1,
  HTTP/2, HTTP/3 and WebSockets, with a console interface (mitmproxy),
  a command-line tool (mitmdump) and a web interface (mitmweb).
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	unzip -q -o $(DL_DIR)/$(PKG_SOURCE) -d $(PKG_BUILD_DIR)
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/mitmproxy/install
	$(INSTALL_DIR) $(1)$(PYTHON3_PKG_DIR) $(1)/usr/bin
	$(CP) $(PKG_BUILD_DIR)/mitmproxy $(PKG_BUILD_DIR)/mitmproxy-$(PKG_VERSION).dist-info \
		$(1)$(PYTHON3_PKG_DIR)/
	for tool in mitmproxy mitmdump mitmweb; do \
		printf '#!/usr/bin/python3\nimport sys\nfrom mitmproxy.tools.main import %s\nsys.exit(%s())\n' \
			$$$$tool $$$$tool > $(1)/usr/bin/$$$$tool; \
		chmod 0755 $(1)/usr/bin/$$$$tool; \
	done
endef

$(eval $(call BuildPackage,mitmproxy))
