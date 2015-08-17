# Maintainer: Mariano Iglesias <mgiglesias@gmail.com>
pkgname=snakefire
pkgver=1.0.6
pkgrel=1
pkgdesc='A Campfire desktop client'
arch=('i686' 'x86_64' 'ppc')
url='http://snakefire.org'
license=('MIT')
depends=('python2' 'python2-pyqt4' 'python2-keyring' 'python2-notify' 'python2-pyfire' 'python2-dbus')
optdepends=('python2-gnomekeyring: For GNOME/XFCE/LXDE users that require notifications' 'python2-pyenchant: For spell checking support')
makedepends=('python2' 'python2-distribute')
source=(http://snakefire.org/downloads/$pkgname-$pkgver.tar.gz)
md5sums=('26e09301f101a91473d060cb2d93da5f')

build() {
    cd "$srcdir/$pkgname-$pkgver"
    python2 setup.py build
}

package() {
    cd "$srcdir/$pkgname-$pkgver"
    python2 setup.py install -O1 --skip-build --install-menu-in-user-mode --root="$pkgdir"
}
