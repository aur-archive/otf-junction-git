# Contributor: Martin Florén <martin.floren@gmail.com>
# Contributor: Ignas Anikevičius <anikevicius@gmail.com>

_pkgname=junction
pkgname=otf-${_pkgname}-git
pkgver=fb73260
pkgrel=1
pkgdesc="A humanist sans-serif typeface"
arch=('any')
url="http://theleagueofmoveabletype.com/junction/"
license=('OFL')
depends=('fontconfig' 'xorg-font-utils')
replaces=('otf-junction')
conflicts=('otf-junction')

install=otf.install
source=($pkgname::git+http://github.com/theleagueof/junction.git)
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  git describe --always | sed 's|-|.|g'
}

package() {
    cd $pkgname
    install -Dm644 "Junction-bold.otf"    "$pkgdir"/usr/share/fonts/OTF/Junction-bold.otf
    install -Dm644 "Junction-light.otf"   "$pkgdir"/usr/share/fonts/OTF/Junction-light.otf
    install -Dm644 "Junction-regular.otf" "$pkgdir"/usr/share/fonts/OTF/Junction-regular.otf
}
