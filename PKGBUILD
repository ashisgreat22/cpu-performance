# Maintainer: ashisgreat22 <ashisgreat39@gmail.com>
pkgname='cpu-performance'
pkgver=1.2.0
pkgrel=1
pkgdesc="Simple script to set CPU governor to performance for all cores, with optional systemd service"
arch=('x86_64')
url="https://github.com/ashisgreat22/cpu-performance"
license=('MIT')
depends=('bash' 'coreutils')
source=("https://github.com/ashisgreat22/cpu-performance/releases/download/v$pkgver/cpu-performance"
        "https://github.com/ashisgreat22/cpu-performance/releases/download/v$pkgver/cpu-performance.service"
        "https://github.com/ashisgreat22/cpu-performance/releases/download/v$pkgver/cpu-performance.conf")
sha256sums=('4b479990f47870b9b64e34fe7200e23a1a3a9640793d6ee342e126cbb9152e61'
            '26c9a6ec7029a7d7d952506b09786a145b1a03d2c6f8c9b1a384d5977d280db9'
            'deaf0548b8e89eb5fe3da26cdbfa9a7851f4c4c1a7c753dfe60b4b17444f51ca')

package() {
  install -Dm755 "$srcdir/cpu-performance" "$pkgdir/usr/bin/cpu-performance"
  install -Dm644 "$srcdir/cpu-performance.service" "$pkgdir/usr/lib/systemd/system/cpu-performance.service"
  install -Dm644 "$srcdir/cpu-performance.conf" "$pkgdir/etc/cpu-performance.conf"
}
