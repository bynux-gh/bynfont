# Maintainer: Bryn Miller <bryn@brynmiller.me>
pkgname="bynfont"
pkgver=1.0.0
pkgrel=1
pkgdesc="A bitmap font for Linux console that combines other fonts' best features."
arch=("any")
url="https://github.com/bynux-gh/bynfont"
license=('GPL')
depends=()
makedepends=()
optdepends=()
source=("git+${url}.git#tag=${_tag}?signed")
md5sums=("SKIP")
validpgpkeys=(BE6845F602EA82F24A81EAE66D56E565881BDA42)

_sourceName="bynfont"
pkgver() {
  cd "${_sourceName}"
  git describe --tags | sed 's/^v//'
}

package() {
  cd "${_sourceName}"
  install -Dm 644 LICENSE -t "${pkgdir}"/usr/share/licenses/"${pkgname}"/
  install -Dm 644 bynfont.psfu.gz -t "${pkgdir}"/usr/share/kbd/consolefonts/"${pkgname}"/
}
