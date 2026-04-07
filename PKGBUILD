pkgname=urxvt-tabbedex
pkgver=26.15
pkgrel=1

pkgdesc="Tabbed plugin for rxvt-unicode with many enhancements "
url='https://github.com/mina86/urxvt-tabbedex'
arch=("any")
license=("GPL-3.0-or-later")
depends=('rxvt-unicode')
makedepends=('perl')
install=urxvt-tabbedex.install
# https://github.com/mina86/$pkgname/archive/v$pkgver.tar.gz
source=(https://github.com/mina86/$pkgname/releases/download/v$pkgver/$pkgname-$pkgver.tar.bz2
        urxvt-tabbedex.install)

sha256sums=('a8377fb12f73b7c9e235d28a222a210c92e5cefb53366ffcde7e9f10daec29c0'
            '7f723f5e3509e96fab53f1653b647947ee0350dc92127c9c3e7c2579dbcd4658')

build() {
	# Make sure PATH is updated to include pod2man.
	which pod2man >/dev/null 2>&1 || source /etc/profile
	make -C "$srcdir/$pkgname-$pkgver"
}

package() {
	make -C "$srcdir/$pkgname-$pkgver" DESTDIR="$pkgdir" install
}
