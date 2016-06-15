pkgname=jdupes
pkgver=1.2.1
pkgrel=1
pkgdesc="A powerful duplicate file finder and an enhanced fork of 'fdupes'. "
arch=('x86_64')
url="https://kaosx.us"
license=('MIT')
source=(${pkgname}-${pkgver}.tar.gz::"https://github.com/jbruchon/${pkgname}/archive/v${pkgver}.tar.gz")
sha512sums=('974b3b12e2bc8078ac4e48d4f7aec53292102c34e36bfbc1ecd1e83dd9e99f464e0d5ce95ccbd64bf99086f6a73a064da346a59933283fa86a561182b38b92cb')

build() {
 cd "${pkgname}-${pkgver}"
 make
}

package() {
 cd "${pkgname}-${pkgver}"
 install -d "${pkgdir}"/usr/{share/man/man1,bin}
 make DESTDIR="${pkgdir}/" install
}
