# Maintainer: Jeremy Goss <jem@goss-family.net>

pkgbase=bluez-utils
pkgname=bluetoothctl
pkgver=5.77
pkgrel=1
pkgdesc="Just the bluetoothctl program from bluez-utils"
url="http://www.bluez.org/"
arch=('x86_64')
license=('GPL2')

pkgfile="$pkgbase-$pkgver-$pkgrel-$arch.pkg.tar.zst"
source=("$pkgfile::https://archlinux.org/packages/extra/$arch/$pkgbase/download")
sha256sums=('4ac0dfda19390dcbc0c8321cfc52b6068fd984f8299c53c322bcbca306b36673')
noextract=("$pkgfile")

check() {
  echo "Checking..."
  [[ "$(pacman -Qp $pkgfile)" == "$pkgbase $pkgver-$pkgrel" ]]
}

package() {
  tar xf "$srcdir"/$pkgfile -C $pkgdir usr/bin/bluetoothctl
}
