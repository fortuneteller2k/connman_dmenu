pkgname=connman-dmenu-rootless
pkgver=60.0595a14
pkgrel=1
pkgdesc="connman dmenu frontend (rootless)"
arch=('any')
url="https://github.com/fortuneteller2k/connman_dmenu"
license=('GPL3')
depends=('bash' 'connman' 'dmenu' 'dnsutils')
makedepends=('git')
conflicts=('connman_dmenu-git')
provides=('connman_dmenu-git')
source=("git://github.com/taylorchu/connman_dmenu.git")
md5sums=('SKIP')

_gitroot="connman_dmenu"

pkgver () {
    cd "$srcdir/$_gitroot"
    echo "$(git rev-list --count HEAD).$(git describe --always)"
}

package() {
    cd "$srcdir/$_gitroot"
    make PREFIX=/usr DESTDIR="$pkgdir" install
}
