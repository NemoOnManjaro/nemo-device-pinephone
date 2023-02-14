## $Id$
# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>

_basename=nemo-device-dont_be_evil
pkgname=nemo-device-pinephone

pkgver=0.13.1
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
sha256sums=('3b8df7ed2d0d30d9e9692b85c1a7ec07934763a27d0043d61ed8ae9df8ca5422')

package() {
    mkdir -p ${pkgdir}
    cp -r $_basename-$pkgver/sparse/* ${pkgdir}/
    sed -r "s/NEMOVER/${pkgver}/" $_basename-$pkgver/sparse/etc/hw-release > ${pkgdir}/etc/hw-release
}
