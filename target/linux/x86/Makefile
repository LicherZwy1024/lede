# SPDX-License-Identifier: GPL-2.0-only
#
# Copyright (C) 2006-2011 OpenWrt.org

include $(TOPDIR)/rules.mk

ARCH:=i386
BOARD:=x86
BOARDNAME:=x86
FEATURES:=squashfs vdi vmdk pcmcia fpu
SUBTARGETS:=64 generic zen legacy geode 
MAINTAINER:=Felix Fietkau <nbd@nbd.name>

KERNEL_PATCHVER:=5.4
KERNEL_TESTING_PATCHVER:=5.10

KERNELNAME:=bzImage

include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES += partx-utils mkf2fs fdisk e2fsprogs wpad kmod-usb-hid kmod-mmc-spi kmod-sdhci \
kmod-ath5k kmod-ath9k kmod-ath9k-htc kmod-ath10k kmod-rt2800-usb kmod-e1000e kmod-igb kmod-igc kmod-igbvf kmod-ixgbe kmod-pcnet32 kmod-tulip kmod-vmxnet3 kmod-i40e kmod-i40evf kmod-r8125 kmod-8139cp kmod-8139too kmod-fs-f2fs \
htop lm-sensors autocore-x86 automount autosamba luci-app-adbyby-plus luci-app-ipsec-vpnd luci-proto-bonding luci-app-unblockmusic luci-app-zerotier luci-app-xlnetacc ddns-scripts_aliyun ddns-scripts_dnspod ca-certificates luci-app-jd-dailybonus luci-app-uugamebooster \
ath10k-firmware-qca988x ath10k-firmware-qca9888 ath10k-firmware-qca9984 brcmfmac-firmware-43602a1-pcie \
kmod-sound-hda-core kmod-sound-hda-codec-realtek kmod-sound-hda-codec-via kmod-sound-via82xx kmod-sound-hda-intel kmod-sound-hda-codec-hdmi kmod-sound-i8x0 kmod-usb-audio \
kmod-usb-net kmod-usb-net-asix kmod-usb-net-asix-ax88179 kmod-usb-net-rtl8150 kmod-usb-net-rtl8152-vendor kmod-r8168 kmod-mlx4-core kmod-mlx5-core kmod-drm-amdgpu \
-luci-app-sfe luci-app-flowoffload

$(eval $(call BuildTarget))

$(eval $(call $(if $(CONFIG_TARGET_ROOTFS_ISO),RequireCommand,Ignore),mkisofs, \
   	Please install mkisofs. \
))
