pkgname=gitkraken
pkgver=6.4.1
pkgrel=1
pkgdesc="Git client with efficiency, elegance and reliability at the core"
arch=('x86_64')
url="https://www.gitkraken.com/"
license=('custom: https://www.gitkraken.com/eula')
depends=('curl-kcp' 'gtk2' 'nss' 'libxtst' 'libnotify' 'alsa-lib' 'libsecret')
optdepends=('openssh' 'gnupg')
source=("https://release.gitkraken.com/linux/GitKraken-v$pkgver.tar.gz"
        "${pkgname}.desktop"
        "${pkgname}.svg"
        "${pkgname}.sh")
md5sums=('383079c5caf9862bdccfddea2cce2767'
         'e70ed2fa89e0929c02262f9300f0f1b2'
         '952efc24804093bec7a95efe02d18c48'
         '10af5f5f6e5253f3b742982ebde6c1ae')

package() {
    install -dm755 ${pkgdir}/opt/${pkgname} \
            ${pkgdir}/usr/share/{applications,icons/hicolor/scalable/apps} \
            ${pkgdir}/usr/bin
    cp -R ${srcdir}/${pkgname}/* ${pkgdir}/opt/${pkgname}
    install -Dm755 ${srcdir}/${pkgname}.sh ${pkgdir}/usr/bin/${pkgname}
    install -Dm644 ${srcdir}/${pkgname}.desktop \
            ${pkgdir}/usr/share/applications/${pkgname}.desktop
    install -Dm644 ${srcdir}/${pkgname}.svg \
            ${pkgdir}/usr/share/icons/hicolor/scalable/apps/${pkgname}.svg
}
