1.取消开源驱动：kmod-mt7603、kmod-mt7615-fireware和 kmod-mt7615e，以及wpad-openssl （network-wirelessAPD下面，可能是wpad-mini或其他的，总之把wpad开头的都取消否则会冲突

2.选择闭源驱动：mtwifi、kmod-mt7603e、kmod-mt7615d

scp /tmp/157.config  root@host:/tmp/


scp  root@host:/tmp/tt.config .config



Extra packages---ipv6helper 

# Open source WIFI driver 
CONFIG_PACKAGE_kmod-mt7603=y

CONFIG_PACKAGE_kmod-mt7603e=n

CONFIG_PACKAGE_kmod-mt76x2=y

CONFIG_PACKAGE_kmod-mt76x2e=n

CONFIG_PACKAGE_hostapd-common=y

CONFIG_PACKAGE_wpad-openssl=y

CONFIG_PACKAGE_luci-app-mtwifi=n

make package/luci-theme-rosy/luci-theme-rosy/compile V=99
svn checkout https://github.com/AmadeusGhost/lede/branches/ramips/target/linux/ramips
