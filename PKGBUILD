# Maintainer: Rafael <rafael@rebornos.org>
# PKGBUILD modified for use with Github code

pkgname=new-cnchi
codename=new-cnchi-code
lname=locale
ccommit=b207da033c6c5f6db42754912790f12c152ab84a
lcommit=c3d06a98b584e533537d022995a1bba1477b78ba
pkgver=20211011
pkgrel=1
pkgdesc='New cnchi code installer'
arch=('any')
url='https://github.com/RebornOS-Developers'
license=('GPL3')
depends=(git)
source=("git+${url}/${codename}#commit=${ccommit}"
        "git+${url}/${lname}#commit=${lcommit}")
sha256sums=('SKIP' 'SKIP')
       
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

