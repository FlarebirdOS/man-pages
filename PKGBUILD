pkgname=man-pages
pkgver=6.17
pkgrel=3
pkgdesc="Linux man pages"
arch=('x86_64')
url="https://www.kernel.org/doc/man-pages"
license=('BSD-2-Clause'
    'BSD-3-Clause'
    'BSD-4.3TAHOE'
    'BSD-4-Clause-UC'
    'GPL-1.0-or-later'
    'GPL-2.0-only'
    'GPL-2.0-or-later'
    'GPL-3.0-or-later'
    'LGPL-3.0-or-later'
    'LGPL-3.0-linking-exception'
    'LicenseRef-Public-Domain'
    'LicenseRef-UltraPermissive'
    'Linux-man-pages-1-para'
    'Linux-man-pages-copyleft'
    'Linux-man-pages-copyleft-2-para'
    'Linux-man-pages-copyleft-var'
    'MIT'
    'Spencer-94')
source=(https://www.kernel.org/pub/linux/docs/${pkgname}/${pkgname}-${pkgver}.tar.xz)
sha256sums=(d18f21a602b09778a5a9096bf1be8441b7733e998150474accf703d165f4ebf4)

prepare() {
    cd ${pkgname}-${pkgver}

    rm -v man3/crypt*
}

package() {
    cd ${pkgname}-${pkgver}

    make -R GIT=false prefix=${pkgdir}/usr install
}
