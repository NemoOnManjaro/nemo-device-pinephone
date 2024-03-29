## $Id$
# Maintainer: Chupligin Sergey (NeoChapay) <neochapay@gmail.com>

_basename=nemo-device-dont_be_evil
pkgname=nemo-device-pinephone

pkgver=0.14
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
    'libqofono-qt6'
    'glacier-dialer'
    'glacier-pinquery'
    'qt6-sensors-sensorfw'
    'libngf-qt6'
    'qt-mobility-haptics-ffmemless'
    'bluez-utils>5.44'
    'gpsd'
    'atinout'
    'eg25-manager'
    'pulseaudio-module-keepalive'
    'buteo-mtp')

conflicts=("usb-tethering")
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('510cc28c6500348087d6532d66a6c66ffa7cee8b6711e1fd93ce1a8777a7ba8a')

package() {
    mkdir -p ${pkgdir}
    cp -r $_basename-$pkgver/sparse/* ${pkgdir}/
    sed -r "s/NEMOVER/${pkgver}/" $_basename-$pkgver/sparse/etc/hw-release > ${pkgdir}/etc/hw-release
}
