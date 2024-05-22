#
# Copyright (C) 2023 CZ.NIC z. s. p. o. (https://www.nic.cz/)
#
# This is free software, licensed under the GNU General Public License v3.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=reforis-{{cookiecutter.name}}-plugin
PKG_VERSION:={{cookiecutter.version}}
PKG_RELEASE:=$(AUTORELEASE)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:={{cookiecutter.repo_url}}
PKG_MIRROR_HASH:=
PKG_SOURCE_VERSION:=v$(PKG_VERSION)

PKG_MAINTAINER:=CZ.NIC <packaging@turris.cz>
PKG_LICENSE:=GPL-3.0-or-later
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=\
	node/host \

PYTHON3_PKG_WHEEL_NAME:=reforis_{{cookiecutter.name_snake}}

include $(INCLUDE_DIR)/package.mk
include $(TOPDIR)/feeds/packages/lang/python/python3-package.mk
include ../reforis/files/reforis-plugin.mk
include ../reforis/files/reforis-translations.mk

define Package/reforis-{{cookiecutter.name}}-plugin
  SECTION:=web
  CATEGORY:=Web
  SUBMENU:=reForis
  TITLE:=reForis {{cookiecutter.name}} plugin
  URL:={{cookiecutter.repo_url}}
  DEPENDS:=\
    +reforis
endef

define Package/reforis-{{cookiecutter.name}}-plugin/description
  {{cookiecutter.description}}
endef

REFORIS_TRANSLATIONS:=cs

$(eval $(call ReForisPlugin,reforis-{{cookiecutter.name}}-plugin,reforis_{{cookiecutter.name_snake}}))
# call BuildPackage <= assures OWR build system that this is package
