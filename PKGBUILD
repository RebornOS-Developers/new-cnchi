# Maintainer: Rafael <rafael@rebornos.org>
# PKGBUILD modified for use with Github code

pkgname=new-cnchi
codename=new-cnchi-code
lname=locale
commit1=16e61b536babf6a96b99f01a2358adc581b3f8ef
commit2=c3d06a98b584e533537d022995a1bba1477b78ba
pkgver=20211009
pkgrel=1
pkgdesc='New cnchi code installer'
arch=('any')
url='https://github.com/RebornOS-Developers'
license=('GPL3')
source=("git+${url}/${codename}#commit=${commit1}"
        "git+${url}/${lname}#commit=${commit2}")
sha256sums=('SKIP'
            'SKIP')
            
pkgver() {
    date +%Y%m%d
}

package() {
    install -d ${pkgdir}/usr/share/cnchi
    install -d ${pkgdir}/usr/share/locale
    cp -r ${srcdir}/${codename}/* ${pkgdir}/usr/share/cnchi
    cp -r ${srcdir}/${lname}/${lname}/* ${pkgdir}/usr/share/${lname}
    find ${pkgdir}/usr/share/cnchi -type f -exec chmod 644 {} \;
    find ${pkgdir}/usr/share/locale -type f -exec chmod 644 {} \;
    find ${pkgdir}/usr/share/cnchi -type d -exec chmod 755 {} \;
    find ${pkgdir}/usr/share/locale -type d -exec chmod 755 {} \;
    }

