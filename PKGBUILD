pkgname=uchardet
pkgver=0.0.1
pkgrel=1
pkgdesc="An encoding detector library"
arch=('x86_64')
url="http://code.google.com/p/uchardet/"
license=('MPL')
makedepends=('cmake')
source=("http://uchardet.googlecode.com/files/$pkgname-$pkgver.tar.gz")
md5sums=('9c17f0aca38c66c95d400691a9160b1b')

build() {
  cd "$srcdir/$pkgname-$pkgver"
	cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release
  make
}

check() {
  cd "$srcdir/$pkgname-$pkgver"
  #make -k check
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}
