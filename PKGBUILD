# Maintainer: EMPTY <testerthe60@gmail.com>
pkgname=portmaster-runit
pkgver=v0.7.0
pkgrel=1
pkgdesc="Portmaster runit service (does not include portmaster itself)"
arch=("any")
url="https://github.com/0x454d505459/portmaster-runit.git"
license=('GPLv3')
groups=()
# depends=("portmaster")
source=("$pkgname-$pkgver-$pkgrel.tar.gz::https://github.com/0x454d505459/$pkgname/releases/download/$pkgver/$pkgver.tar.gz")
md5sums=()

package() {
    mkdir "/etc/runit/sv/portmaster"
    mv $srcdir/run /etc/runit/sv/portmaster/run
    chmod 755 /etc/runit/sv/portmaster /etc/runit/sv/portmaster/run
    ln -s /etc/runit/sv/portmaster /run/runit/service/portmaster
}
