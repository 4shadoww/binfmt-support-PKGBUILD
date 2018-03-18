# Maintainer: Noa-Emil Nissinen <aur dot satella at spamgourmet dot org>
pkgname=binfmt-support
pkgver=2.1.8
pkgrel=1
pkgdesc="Provides an update-binfmts script"
arch=("any")
url="http://binfmt-support.nongnu.org/"
license=('GPL 3')
makedepends=()
source=("https://git.savannah.gnu.org/cgit/binfmt-support.git/snapshot/$pkgname-$pkgver.tar.gz")
md5sums=(93401f2ff27acd7be544e5463d9109f7)

build() {
	cd "$pkgname-$pkgver"
	./configure --prefix=/usr --sbindir=/usr/bin
	make
}

check() {
	cd "$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
