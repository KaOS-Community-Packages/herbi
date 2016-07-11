pkgname=herbi
pkgver=0.9
pkgrel=1
_pkgname=Herbi
pkgdesc="A retro platformer which you have to collect all diamonds"
arch=('x86_64')
url="http://kobuge-games.github.io/Herbi/"
license=('MIT')
depends=('godot')
source=("https://github.com/KOBUGE-Games/Herbi/archive/v${pkgver}.tar.gz"
        'herbi.desktop'
        'launch-herbi.sh')
md5sums=('e007b9628c28a783cf56e454544a9043'
         '66ddb43f04afc56866160d55513faa02'
         '67c563f4a59e0a879586896cfd1745e4')

package() {
    cd ${_pkgname}-${pkgver}
    
    install -d ${pkgdir}/opt/herbi
    cp -r * ${pkgdir}/opt/herbi/
    chmod 755 -R ${pkgdir}/opt/herbi
    
    install -Dm755 ${srcdir}/launch-herbi.sh ${pkgdir}/usr/bin/launch-herbi.sh
    install -Dm644 $srcdir/herbi.desktop ${pkgdir}/usr/share/applications/herbi.desktop
    install -Dm644 ${srcdir}/${_pkgname}-${pkgver}/icon.png ${pkgdir}/usr/share/pixmaps/herbi.png
}
