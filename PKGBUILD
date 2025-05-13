# Maintainer: ashisgreat22 <ashisgreat39@gmail.com>
pkgname='cpu-performance'
pkgver=1.0.1
pkgrel=1
pkgdesc="Simple script to set CPU governor to performance for all cores"
arch=('x86_64')
url="https://github.com/ashisgreat22/cpu-performance"
license=('MIT')
depends=('bash' 'coreutils')
source=("https://github.com/ashisgreat22/cpu-performance/releases/download/v$pkgver/cpu-performance")
sha256sums=('cfa1c23a993d8dec49e1c4091a337e4d58f1ae34c80caf63df66ad99b1ef2eac')

package() {
  install -Dm755 "$srcdir/cpu-performance" "$pkgdir/usr/bin/cpu-performance"
}
