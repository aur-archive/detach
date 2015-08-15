# Maintainer: Limao Luo <luolimao+AUR@gmail.com>

pkgname=detach
pkgver=0.2.0
pkgrel=3
pkgdesc="Starts a program by detaching it from the running terminal."
arch=(i686 x86_64)
url=http://detach.sourceforge.net/
license=(GPL2)
source=(http://downloads.sourceforge.net/$pkgname/$pkgname-$pkgver.tar.gz)
sha256sums=('57fb8c8e46a6a5c2b2e72d1d921f1afc0807ff76d2bf145891c9a9ad1ad736b0')
sha512sums=('609fd6127927d3ab80d5106e45afee08532bf7094e73b69ae806532c24e11fdff7ed42247d40edefb20eefffe12e4208b19a53fbc85514320ff0e1cfddea8f76')

build() {
    cd $pkgname-$pkgver/
    ./configure --prefix=/usr
    make
}

package() {
    make -C $pkgname-$pkgver DESTDIR="$pkgdir" install
}
