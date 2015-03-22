# Maintainer: Lars Christensen <larsch at belunktum dk>
# Contributor: Arne Ko arneko {a t} yahoo . com

_pkgbasename=bcm2835
pkgname=libbcm2835
pkgver=1.42
pkgrel=1
pkgdesc="C library for Broadcom BCM 2835 as used in Raspberry Pi"
arch=('armv6h' 'armv7h')
url="http://www.open.com.au/mikem/bcm2835/"
license=('GPL')
depends=('')
makedepends=()
options=('staticlibs')
source=('http://www.airspayce.com/mikem/bcm2835/bcm2835-1.42.tar.gz' 'bcm2835.patch')
md5sums=('3f60ac30ada6b8f7036243f13da441ba'
         '62085703dbef25ed501002dec077c3d5')

prepare() {
    ls
    patch -p0 -i "$srcdir/bcm2835.patch"
}

build() {
    cd "$srcdir/bcm2835-1.42"
    ./configure --prefix=/usr
    make
}

package() {
    cd "$srcdir/bcm2835-1.42"
    make DESTDIR="$pkgdir" install
}

