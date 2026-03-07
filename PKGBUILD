# Maintainer: Antonio Rojas <arojas@archlinux.org>

pkgbase=noto-fonts-cjk
pkgname=(ttf-noto-fonts-cjk otf-noto-fonts-cjk)
_sans_ver=2.004
_serif_ver=2.003
pkgver=20240730
pkgrel=2
pkgdesc='Google Noto CJK fonts'
arch=(any)
url='https://fonts.google.com/noto'
license=(OFL-1.1)
source=(
  "https://github.com/notofonts/noto-cjk/releases/download/Sans${_sans_ver}/03_NotoSansCJK-OTC.zip"
  "https://github.com/notofonts/noto-cjk/releases/download/Serif${_serif_ver}/04_NotoSerifCJKOTC.zip"
  "https://github.com/notofonts/noto-cjk/releases/download/Sans${_sans_ver}/04_NotoSansCJK-OTF.zip"
  "https://github.com/notofonts/noto-cjk/releases/download/Serif${_serif_ver}/05_NotoSerifCJKOTF.zip"
)
b2sums=(
  '6e86b4c3f1a027833e129aa510a15e642c534526f703fe71de6ef1db066c71661289ecce06864a77179d9c84fd625430ea5d81c7f75d9187be03207cadf4d1be'
  '7e9d7cfbe97ce6f2b7246b3d177ff1487f79aa2b2cba957a13ca2aac6510a262ebaa60c34ccd3a1695cedc7e43535d1706086a8e6bfa2dfe84d365d55b7ac75b'
  'e9bea5c35be61409953c04757f73e809b4781d70e9a49d42b0f8a2d7ea339c2ababda02de3ebc1e0992b6f646996563e85ae3316e11ab41df0e36702373ae5fa'
  '9789ba636479119f23944a831a8b78ce870a49ce029c9a62b31a04c4191e99165854232eb2591e83925d7fe2745529f50d197f01d69db682547e31f96c07f325'
)

package_ttf-noto-fonts-cjk() {
  provides=(noto-fonts-cjk)
  conflicts=(noto-fonts-cjk)
  replaces=(noto-fonts-cjk)

  find "${srcdir}" \( -iname '*.ttf' -o -iname '*.ttc' \) -exec install -D -m644 -t "${pkgdir}/usr/share/fonts/${pkgbase//-fonts/}" {} +
  install -D -m644 "${srcdir}/LICENSE" -t "${pkgdir}/usr/share/licenses/${pkgname}"
}

package_otf-noto-fonts-cjk() {
  provides=(noto-fonts-cjk)
  conflicts=(noto-fonts-cjk)

  find "${srcdir}" -iname '*.otf' -exec install -D -m644 -t "${pkgdir}/usr/share/fonts/${pkgbase//-fonts/}" {} +
  install -D -m644 "${srcdir}/LICENSE" -t "${pkgdir}/usr/share/licenses/${pkgname}"
}
