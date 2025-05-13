# Maintainer: ashisgreat22 <ashisgreat39@gmail.com>
pkgname='cpu-performance'
pkgver=1.1.0
pkgrel=1
pkgdesc="Simple script to set CPU governor to performance for all cores, with optional systemd service"
arch=('x86_64')
url="https://github.com/ashisgreat22/cpu-performance"
license=('MIT')
depends=('bash' 'coreutils')
source=("https://github.com/ashisgreat22/cpu-performance/releases/download/v$pkgver/cpu-performance" "https://github.com/ashisgreat22/cpu-performance/releases/download/v$pkgver/cpu-performance.service")
sha256sums=('5b46bec172c555fefbe6bc2cf4fffb6ba2b71b45d29333559b808ee1ce650f97'
            '26c9a6ec7029a7d7d952506b09786a145b1a03d2c6f8c9b1a384d5977d280db9')

package() {
  install -Dm755 "$srcdir/cpu-performance" "$pkgdir/usr/bin/cpu-performance"
  install -Dm644 "$srcdir/cpu-performance.service" "$pkgdir/usr/lib/systemd/system/cpu-performance.service"
}
