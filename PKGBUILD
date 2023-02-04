## $Id$
# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>

_basename=nemo-device-dont_be_evil
pkgname=nemo-device-pinephone

pkgver=0.13
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
sha256sums=('ddc4596c12a0a6204de93783ac2812e68e6fa6299823e057c0a34346ec5dd148')

package() {
    mkdir -p ${pkgdir}
    cp -r $_basename-$pkgver/sparse/* ${pkgdir}/
    sed -r "s/NEMOVER/${pkgver}/" $_basename-$pkgver/sparse/etc/hw-release > ${pkgdir}/etc/hw-release
}
