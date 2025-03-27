# Maintainer: Jeremy Goss <jem@goss-family.net>

pkgbase=bluez-utils
pkgname=bluetoothctl
pkgver=5.80
pkgrel=1
pkgdesc="Just the bluetoothctl program from bluez-utils"
url="http://www.bluez.org/"
arch=('x86_64')
license=('GPL2')

pkgfile="$pkgbase-$pkgver-$pkgrel-$arch.pkg.tar.zst"
source=("$pkgfile::https://archlinux.org/packages/extra/$arch/$pkgbase/download")
sha256sums=('01eedc0f35c8685530d2994aa50c7a5ad992b5ed2011d8acc01b598161972b09')
noextract=("$pkgfile")

check() {
  echo "Checking..."
  [[ "$(pacman -Qp $pkgfile)" == "$pkgbase $pkgver-$pkgrel" ]]
}

package() {
  tar xf "$srcdir"/$pkgfile -C $pkgdir usr/bin/bluetoothctl
}
