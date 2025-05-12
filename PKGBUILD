# Maintainer: ashisgreat22 <ashisgreat39@gmail.com>
pkgname='cpu-performance'
pkgver=1.0.0
pkgrel=1
pkgdesc="Simple script to set CPU governor to performance for all cores"
arch=('x86_64')
url="https://github.com/ashisgreat22/cpu-performance"
license=('MIT')
depends=('bash' 'coreutils')
source=("https://github.com/ashisgreat22/cpu-performance/releases/download/v$pkgver/cpu-performance")
sha256sums=('20f8d3aea37a534acbd9b698e8a798960e70c8ea4d67c21015ee3b24b8ee7a69')

package() {
  install -Dm755 "$srcdir/cpu-performance" "$pkgdir/usr/bin/cpu-performance"
}
