## $Id$
# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>

_basename=nemo-device-dont_be_evil
pkgname=nemo-device-pinephone

pkgver=0.13.2
pkgrel=1
pkgdesc="PinePhone specific files for GlacierUX"
arch=('aarch64')
url="https://github.com/neochapay/$_basename"
license=('BSD-3-Clause')
depends=('glacier-wayland-session'
	'usb-moded'
	'maliit-nemo-keyboard'
	'sensorfw'
	'ofono'
	'ofonoctl'
	'libqofono-qt5'
	'glacier-dialer'
	'glacier-pinquery'
	'qt5-sensors-sensorfw'
	'libngf-qt'
	'qt-mobility-haptics-ffmemless'
	'bluez-utils>5.44'
	'gpsd'
	'atinout'
	'eg25-manager'
	'pulseaudio-module-keepalive'
	'buteo-mtp')

conflicts=("usb-tethering")
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('3abeeb87d5b79ec0dc5d9b424dd19edaa910e085e4d57bd6d6645c907f69e5ea')

package() {
    mkdir -p ${pkgdir}
    cp -r $_basename-$pkgver/sparse/* ${pkgdir}/
    sed -r "s/NEMOVER/${pkgver}/" $_basename-$pkgver/sparse/etc/hw-release > ${pkgdir}/etc/hw-release
}
