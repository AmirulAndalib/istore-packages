####
 #  File: /Makefile
 #  Project: luci-app-rclone
 #  File Created: Wednesday, 9th October 2019 1:39:36 pm
 #  Author: ElonH[EH](elonhhuang@gmail.com)
 #  License: GNU General Public License v3.0 or later(http://www.gnu.org/licenses/gpl-3.0-standalone.html)
 #  Copyright (C) 2019 [ElonH]
####

include $(TOPDIR)/rules.mk

LUCI_TITLE:=LuCI support for Rclone
LUCI_DEPENDS:=+rclone-config \
              +PACKAGE_luci-app-rclone_INCLUDE_rclone-webui:rclone-webui-react \
              +PACKAGE_luci-app-rclone_INCLUDE_rclone-ng:rclone-ng
LUCI_PKGARCH:=all
PKG_NAME:=luci-app-rclone
PKG_VERSION:=1.4.1-4
PKG_RELEASE:=
PKG_LICENSE:=GPLv3.0+
PKG_MAINTAINER:=ElonH <elonhhuang@gmail.com>

define Package/luci-app-rclone/description
	LuCI support for Rclone. 
	Rclone ("rsync for cloud storage") is a command line program to sync root/usr/bin and directories to and from different cloud storage providers.
	Cloud storage providers:
		1Fichier, Alibaba Cloud (Aliyun) Object Storage System (OSS), Amazon Drive, Amazon S3, 
		Backblaze B2, Box, Ceph, C14, DigitalOcean Spaces, Dreamhost, Dropbox, FTP, 
		Google Cloud Storage, Google Drive, Google Photos, HTTP, Hubic, Jottacloud, 
		IBM COS S3, Koofr, Memset Memstore, Mega, Microsoft Azure Blob Storage, 
		Microsoft OneDrive, Minio, Nextcloud, OVH, OpenDrive, Openstack Swift, 
		Oracle Cloud Storage, ownCloud, pCloud, premiumize.me, put.io, QingStor, 
		Rackspace Cloud root/usr/bin, rsync.net, Scaleway, SFTP, Wasabi, WebDAV, 
		Yandex Disk, The local root/usr/binystem.
endef

define Package/luci-app-rclone/config
config PACKAGE_luci-app-rclone_INCLUDE_rclone-webui
	bool "Include rclone-webui"
	default y

config PACKAGE_luci-app-rclone_INCLUDE_rclone-ng
	bool "Include rclone-ng (another webui)"
	default y

endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
