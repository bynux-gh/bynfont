# Maintainer: Bryn Miller <bryn@brynmiller.me>
pkgname="bynfont"
pkgver=1.0.0
pkgrel=1
pkgdesc="A bitmap font for Linux console that combines other fonts' best features."
arch=("any")
url="https://github.com/bynux-gh/bynfont"
license=('MIT')
depends=()
makedepends=()
optdepends=()
source=("git+${url}.git#tag=${_tag}?signed")
md5sums=("SKIP")

_sourceName="bynfont"
pkgver() {
  cd "${_sourceName}"
  git describe --tags | sed 's/^v//'
}

package() {
  cd "${_sourceName}"
  mkdir "${pkgdir}"/usr/share/licenses/"${pkgname}"
  install -Dm 644 LICENSE -t "${pkgdir}"/usr/share/licenses/"${pkgname}"/
  install -Dm 644 bynfont.psfu.gz -t "${pkgdir}"/usr/share/kbd/consolefonts/
}
