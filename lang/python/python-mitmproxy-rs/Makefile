# SPDX-License-Identifier: GPL-2.0-only

include $(TOPDIR)/rules.mk

PKG_NAME:=python-mitmproxy-rs
PKG_VERSION:=0.12.15
PKG_RELEASE:=2
PKG_MAINTAINER:=Tim auf der Landwehr <tadl-git@taufderl.de>

PYPI_NAME:=mitmproxy-rs
PYPI_SOURCE_NAME:=mitmproxy_rs
PKG_HASH:=f1e7e3273a4ba25289a8060e2c7b2bca16d0cd59a25f0b61ca94be7938e88327

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=python-maturin/host

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-mitmproxy-rs
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Rust components of mitmproxy
  URL:=https://github.com/mitmproxy/mitmproxy_rs
  DEPENDS:=+python3-light $(RUST_ARCH_DEPENDS)
endef

define Package/python3-mitmproxy-rs/description
  Rust bits of mitmproxy: WireGuard and transparent proxy servers, content
  views and syntax highlighting. Built without mitmproxy-linux (the eBPF
  redirector for local capture mode, which has no 32-bit ARM support).
endef

$(eval $(call Py3Package,python3-mitmproxy-rs))
$(eval $(call BuildPackage,python3-mitmproxy-rs))
$(eval $(call BuildPackage,python3-mitmproxy-rs-src))
