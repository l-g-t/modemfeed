include $(TOPDIR)/rules.mk

PKG_NAME:=modeminfo
PKG_VERSION:=0.3.9
PKG_RELEASE:=1
PKG_MAINTAINER:=Konstantine Shevlakov <shevlakov@132lan.ru>

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  PKGARCH:=all
  SECTION:=net
  CATEGORY:=Network
  SUBMENU:=Telephony
  DEPENDS:=+comgt
  TITLE:=Signal information for 3G/LTE dongle
endef

define Package/$(PKG_NAME)-serial-simcom-a7xxx
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +kmod-usb-acm +atinout
  TITLE:=SIMCOM A7600/A7906 serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-simcom
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:=SIMCOM SIM7600/SIM7906/SIM7912 serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-huawei
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:=HUAWEI serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-quectel
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:=QUECTEL serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-fibocom
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:=FIBOCOM NL668/678 serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-telit
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:= TELIT LN940/T77W678/HP4220 serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-xmm
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-acm +atinout
  TITLE:= FIBOCOM L850/L860 Intel XMM chips serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-mikrotik
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-acm +atinout
  TITLE:= MikroTik R11e-LTE/R11e-LTE6 serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-sierra
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-qualcomm +atinout
  TITLE:= Sierra Wireless EM7455 serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-styx
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:= STYX MG8224 serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-meig
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:= MEIGLink SLM750-R2, SLM820, SLM828 serial addom for modeminfo
endef

define Package/$(PKG_NAME)-serial-dell
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:= Dell DW5821e serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-gosun
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:= Gosuncnwelink GM510 serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-tw
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:= ThinkWill ML7820+ serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-yuge
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:= Yuge CLM920 serial addon for modeminfo
endef

define Package/$(PKG_NAME)-serial-zte
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +kmod-usb-serial-option +atinout
  TITLE:= ZTE MF823/MF823D serial addon for modeminfo
endef


define Package/$(PKG_NAME)-qmi
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +qmi-utils
  TITLE:=QMI addon for modeminfo
endef

define Package/$(PKG_NAME)-telegram
  PKGARCH:=all
  SUBMENU:=Telephony
  DEPENDS:=+modeminfo +telegrambot
  TITLE:= Plugin for telegrambot
endef

define Package/$(PKG_NAME)/description
	Signal information for 3G/LTE dongle
endef

define Package/$(PKG_NAME)/conffiles
	/etc/config/modeminfo
endef


define Build/Prepare
endef

define Build/Configure
endef

define Build/Compile
endef


define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_DIR) $(1)/usr/share/modeminfo
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(INSTALL_DIR) $(1)/etc/config
	$(CP) ./root/usr/bin/* $(1)/usr/bin
	$(CP) ./root/usr/share/modeminfo/mccmnc.dat  $(1)/usr/share/modeminfo
	$(CP) ./root/usr/share/modeminfo/scripts/*.gcom  $(1)/usr/share/modeminfo/scripts/
	$(CP) ./root/usr/share/modeminfo/scripts/ch_to_band  $(1)/usr/share/modeminfo/scripts/
	$(CP) ./root/usr/share/modeminfo/scripts/family.at  $(1)/usr/share/modeminfo/scripts/
	$(CP) ./root/usr/share/modeminfo/scripts/modeminfo  $(1)/usr/share/modeminfo/scripts/
	$(CP) ./root/usr/share/modeminfo/scripts/GENERIC* $(1)/usr/share/modeminfo/scripts/
	$(CP) ./root/etc/config/* $(1)/etc/config
endef

define Package/$(PKG_NAME)-serial-simcom-a7xxx/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/A7XXX* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-simcom/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/SIMCOM* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-huawei/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/HUAWEI* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-quectel/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/QUECTEL* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-fibocom/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/FIBOCOM* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-telit/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/QUALCOMM* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-xmm/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/INTEL* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-mikrotik/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/MIKROTIK* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-sierra/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/SIERRA* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-styx/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/STYX* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-meig/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/MEIGLINK* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-dell/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/DELL* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-gosun/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/GOSUN* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-tw/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/THINKWILL* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-yuge/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/YUGE* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-serial-zte/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo/scripts/ZTE* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-qmi/install
	$(INSTALL_DIR) $(1)/usr/share/modeminfo/scripts
	$(CP) ./root/usr/share/modeminfo-qmi/* $(1)/usr/share/modeminfo/scripts
endef

define Package/$(PKG_NAME)-telegram/install
	$(INSTALL_DIR) $(1)/usr/lib/telegrambot/plugins
	$(CP) ./root/usr/lib/telegrambot/plugins/* $(1)/usr/lib/telegrambot/plugins
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-simcom-a7xxx))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-simcom))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-huawei))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-quectel))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-fibocom))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-telit))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-xmm))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-mikrotik))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-sierra))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-styx))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-meig))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-dell))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-gosun))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-tw))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-yuge))
$(eval $(call BuildPackage,$(PKG_NAME)-serial-zte))
$(eval $(call BuildPackage,$(PKG_NAME)-qmi))
$(eval $(call BuildPackage,$(PKG_NAME)-telegram))
