# Maintainer: Jeremy Goss <jem@goss-family.net>

pkgbase=bluez-utils
pkgname=bluetoothctl
pkgver=5.68
pkgrel=1
pkgdesc="Just the bluetoothctl program from bluez-utils"
url="http://www.bluez.org/"
arch=('x86_64')
license=('GPL2')

pkgfile="$pkgbase-$pkgver-$pkgrel-$arch.pkg.tar.zst"
source=("$pkgfile::https://archlinux.org/packages/extra/x86_64/bluez-utils/download")
sha256sums=('724067506a4b0912ffeb7c8b794a12cce29351aef9b6c745e08464a40a7be1c1')
noextract=("$pkgfile")

check() {
  echo "Checking..."
  [[ "$(pacman -Qp $pkgfile)" == "$pkgbase $pkgver-$pkgrel" ]]
}

package() {
  tar xf "$srcdir"/$pkgfile -C $pkgdir usr/bin/bluetoothctl
}
