_mayaver=2022

pkgname=maya-usd
pkgver=0.10.0
pkgrel=1
pkgdesc='Autodesk Maya Universal Scene Discription Plugin'
arch=('x86_64')
url='https://github.com/Autodesk/maya-usd'
license=('custom')
depends=('maya>=2022.0' 'maya<2023.0')
verid='202106052251-73d6513'
DLAGENTS+=('manual::/usr/bin/echo \ \ Note: Please download the package manually from the official website')
source=("manual://MayaUSD$_mayaver-$verid-$pkgver-1.x86_64.rpm")
sha256sums=('8cb7f7849a0a5673fe90303d47adb1e8deb9fb54d03e54698c9ef48518bac9db')

options=(!strip)

prepare() {
    sed -i "s|<PLUGIN_DIR>|/usr/autodesk/maya$_mayaver/plug-ins/mayausd|g" usr/autodesk/modules/maya/2022/mayausd.mod
    sed -i 's/\$MAYA_PYTHON_VERSION/3/g' usr/autodesk/modules/maya/2022/mayausd.mod
}

package() {
    mkdir -p $pkgdir/usr/autodesk/maya$_mayaver/{modules,plug-ins/mayausd}

    mv usr/autodesk/modules/maya/$_mayaver/mayausd.mod $pkgdir/usr/autodesk/maya$_mayaver/modules/
    mv usr/autodesk/mayausd/maya$_mayaver/"$pkgver"_"$verid"/mayausd/* $pkgdir/usr/autodesk/maya$_mayaver/plug-ins/mayausd/
}
