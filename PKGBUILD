# Maintainer: Geoffroy Carrier <geoffroy.carrier@koon.fr>
# Contributor: congyiwu <congyiwu AT gmail DOT com>
pkgname=json-c
pkgver=0.9
pkgrel=1
pkgdesc="A JSON implementation in C"
url="http://oss.metaparadigm.com/json-c/"
license=("MIT")
arch=('i686' 'x86_64')
depends=('glibc')
source=(http://oss.metaparadigm.com/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('3a13d264528dcbaf3931b0cede24abae')
options=(!libtool)
build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr || return 1
  make || return 1
  make DESTDIR="$pkgdir" install
  install -D COPYING "$pkgdir/usr/share/licenses/json-c/COPYING"
}
