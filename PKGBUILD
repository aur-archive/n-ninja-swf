# Maintainer: Aleksei Lissitsin <aleksei.lissitsin@gmail.com>
pkgname=n-ninja-swf
pkgver=1.4
pkgrel=3
pkgdesc="Metanet's unique 2D puzzle/action platform game. Version 1.4. (standalone swf file playable with gnash)"
arch=('any')
url="http://www.metanetsoftware.com/"
license=('custom')
groups=()
depends=(gnash-gtk)
makedepends=(exe2swf)
provides=()
conflicts=()
replaces=()
source=(http://www.harveycartel.org/metanet/n_v1pc.zip
	${pkgname}.desktop)
md5sums=('f769e67b4b5dc2da9eb833eaf696d766'
         '6b4819a092d1e17dd5015c17eba33432')

build() {
  cd "${srcdir}"
  exe2swf n_v14.exe
}

package() {
  mkdir -p ${pkgdir}/usr/share/licenses/${pkgname}
  install -D -m644 ${srcdir}/license.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  mkdir -p ${pkgdir}/usr/share/${pkgname}
  install -D -m644 ${srcdir}/n_v14.exe.swf ${pkgdir}/usr/share/${pkgname}/${pkgname}.swf
  mkdir -p ${pkgdir}/usr/share/applications
  install -D -m644 ${pkgname}.desktop ${pkgdir}/usr/share/applications/${pkgname}.desktop
}

