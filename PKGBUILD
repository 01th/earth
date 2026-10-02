# Maintainer: 01th <95thru@gmail.com>
pkgname=earth
pkgver=1.0.0
pkgrel=1
pkgdesc="Rotating Earth in the terminal drawn with Unicode Braille"
arch=('any')
url="https://github.com/01th/earth"
license=('MIT')
depends=('python')
options=('!debug')
source=('earth' 'README.md' 'LICENSE')
sha256sums=('SKIP' 'SKIP' 'SKIP')

package() {
    install -Dm755 earth "$pkgdir/usr/bin/earth"
    install -Dm644 README.md "$pkgdir/usr/share/doc/$pkgname/README.md"
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
