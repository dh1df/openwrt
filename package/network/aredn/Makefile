#
# Copyright (C) 2008-2010 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=aredn
PKG_RELEASE:=5

PKG_MAINTAINER:=OVS48 <aredn@ovs48.de>
PKG_LICENSE:=GPL-2.0
FEED:=hanno1

include $(INCLUDE_DIR)/package.mk

define Package/aredn
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=+olsrd +olsrd-mod-watchdog +olsrd-mod-txtinfo +olsrd-mod-nameservice +olsrd-mod-jsoninfo +olsrd-mod-dot-draw +olsrd-mod-arprefresh +luasocket +libuci-lua +kmod-ipip
  PKGARCH:=all
  TITLE:=AREDN package
endef

define Build/Compile
endef

define Package/aredn/install
	$(INSTALL_DIR) $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/aredn_message.sh $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/aredn_postupgrade $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/aredn_sysupgrade $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/firmwarecheck.sh $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/get_boardid $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/get_hardware_mfg $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/get_hardwaretype $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/get_model $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/linkled $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/manager.lua $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/mesh-firewall $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/node-setup $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/nvram-setup $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/olsrd-config $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/olsrd-namechange $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/poe_passthrough $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/recoverymode $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/setpasswd $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/spawn_sysupgrade $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/upgrade_kill_prep $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/upgrade_prepare.sh $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/uploadctlservices $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/usb_passthrough $(1)/usr/local/bin
	$(INSTALL_BIN) ./files/usr/local/bin/wscan $(1)/usr/local/bin

	$(INSTALL_DIR) $(1)/www $(1)/www/cgi-bin $(1)/www/js
	$(INSTALL_BIN) files/www/connected.png $(1)/www
	$(INSTALL_BIN) files/www/js/sorttable-min.js $(1)/www/js
	$(INSTALL_BIN) files/www/js/jquery.canvasjs.min.js $(1)/www/js
	$(INSTALL_BIN) files/www/js/jquery-2.1.4.min.js $(1)/www/js
	$(INSTALL_BIN) files/www/white_on_black.css $(1)/www
	$(INSTALL_BIN) files/www/trash.png $(1)/www
	$(INSTALL_BIN) files/www/qmark.png $(1)/www
	$(INSTALL_BIN) files/www/red_on_black.css $(1)/www
	$(INSTALL_BIN) files/www/donedone.png $(1)/www
	$(INSTALL_BIN) files/www/viz.png $(1)/www
	$(INSTALL_BIN) files/www/notdone.png $(1)/www
	$(INSTALL_BIN) files/www/done.png $(1)/www
	$(INSTALL_BIN) files/www/upgrademode.html $(1)/www
	$(INSTALL_BIN) files/www/cgi-bin/iperf $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/apiprotected $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/setup $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/lqm $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/admin $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/signal $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/vpn $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/ports $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/sysinfo.json $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/status $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/advancedconfig $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/sysinfo $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/api $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/fwinfo $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/mesh $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/supporttool $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/scan $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/cgi-bin/vpnc $(1)/www/cgi-bin
	$(INSTALL_BIN) files/www/about.html $(1)/www
	$(INSTALL_BIN) files/www/disconnected.png $(1)/www
	$(INSTALL_BIN) files/www/alert-circle-outline.png $(1)/www
	$(INSTALL_BIN) files/www/loading.css $(1)/www
	$(INSTALL_BIN) files/www/help.html $(1)/www
	$(INSTALL_BIN) files/www/yellow_on_black.css $(1)/www
	$(INSTALL_BIN) files/www/aredn.css $(1)/www
	$(INSTALL_BIN) files/www/email.png $(1)/www
	$(INSTALL_BIN) files/www/AREDN.png $(1)/www
	$(INSTALL_BIN) files/www/black_on_white.css $(1)/www
	$(INSTALL_BIN) files/www/dot.png $(1)/www
endef

$(eval $(call BuildPackage,aredn))
