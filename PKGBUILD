# Maintainer: Rafael <rafael@rebornos.org>
# PKGBUILD modified for use with Github code

pkgname=new-cnchi
_pkgname2=new-cnchi-code
_pkgname3=locale
commit1=7569051d43d915e140a3b883c0c6d0cfdd503df4
commit2=c3d06a98b584e533537d022995a1bba1477b78ba
pkgver=20210920
pkgrel=2
pkgdesc='New cnchi code installer'
arch=('any')
url='https://github.com/RebornOS-Developers'
license=('GPL3')
source=("git+${url}/${_pkgname2}#commit=${commit1}"
        "git+${url}/${_pkgname3}#commit=${commit2}")
sha256sums=('SKIP'
            'SKIP')
            
pkgver() {
    date +%Y%m%d
}

package() {
    install -d ${pkgdir}/usr/share/cnchi
    install -d ${pkgdir}/usr/share/locale
    cp -r ${srcdir}/${_pkgname2}/* ${pkgdir}/usr/share/cnchi
    cp -r ${srcdir}/${_pkgname3}/${_pkgname3}/* ${pkgdir}/usr/share/${_pkgname3}
    find ${pkgdir}/usr/share/cnchi -type f -exec chmod 644 {} \;
    find ${pkgdir}/usr/share/locale -type f -exec chmod 644 {} \;
    find ${pkgdir}/usr/share/cnchi -type d -exec chmod 755 {} \;
    find ${pkgdir}/usr/share/locale -type d -exec chmod 755 {} \;
    }

