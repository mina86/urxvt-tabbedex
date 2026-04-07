pkgname=urxvt-tabbedex
pkgver=26.15
pkgrel=1

pkgdesc="Tabbed plugin for rxvt-unicode with many enhancements "
url='https://github.com/mina86/urxvt-tabbedex'
arch=("any")
license=("GPL")
depends=('rxvt-unicode')
install=urxvt-tabbedex.install
# https://github.com/mina86/$pkgname/archive/v$pkgver.tar.gz
source=(https://github.com/mina86/$pkgname/releases/download/v$pkgver/$pkgname-$pkgver.tar.bz2
        urxvt-tabbedex.install)

sha256sums=('a8377fb12f73b7c9e235d28a222a210c92e5cefb53366ffcde7e9f10daec29c0'
            'cfa2c90fe409e85d55fb18841b2c0d321856e0f1cd0c1881a8d1ee19f9553835')

package() {
	cd $srcdir/$pkgname-$pkgver
	install -Dm644 tabbedex "$pkgdir"/usr/lib/urxvt/perl/tabbedex
}
