# Maintainer: Jeremy Goss <jem@goss-family.net>

pkgbase=bluez-utils
pkgname=bluetoothctl
pkgver=5.59
pkgrel=2
pkgdesc="Just the bluetoothctl program from bluez-utils"
url="http://www.bluez.org/"
arch=('x86_64')
license=('GPL2')

pkgfile="$pkgbase-$pkgver-$pkgrel-$arch.pkg.tar.zst"
source=("$pkgfile::https://archlinux.org/packages/extra/x86_64/bluez-utils/download")
sha256sums=('ac9ab1343f30289aacb03060394ac2f9bea3c9b30480eaaad0b9b90f4588a4a2')
noextract=("$pkgfile")

check() {
  echo "Checking..."
  [[ "$(pacman -Qp $pkgfile)" == "$pkgbase $pkgver-$pkgrel" ]]
}

package() {
  tar xf "$srcdir"/$pkgfile -C $pkgdir usr/bin/bluetoothctl
}
