# Maintainer: Stefano Capitani <stefanoatmanjarodotorg>

pkgname=manjaro-aur-support
pkgver=0.6
pkgrel=3
pkgdesc="Manjaro AUR support packages"
_check=check-aur
arch=(any)
url=https://github.com/manjaro/packages-community
depends=('yad' 'manjaro-icons')
source=("$pkgname.hook"
    "$pkgname.script"
    "$_check"
    "$_check.desktop"
    'aur-warning.png')
md5sums=('070a8a590e2c64b1272c264b5919d919'
         '67c814ff1d3c10a1358e24bef9043ba8'
         '4e6a4151016ff326f2b073e22b1ebc08'
         'b06f747debd88e456e63ae0b1f4a046b'
         '9ba5e40b801da994a909ae5fc1a36d24')

package() {
    install -Dm644 manjaro-aur-support.hook $pkgdir/usr/share/libalpm/hooks/manjaro-aur-support.hook
    install -Dm755 manjaro-aur-support.script $pkgdir/usr/share/libalpm/scripts/manjaro-aur-support
    install -Dm755 $_check $pkgdir/usr/bin/$_check
    install -Dm644 $_check.desktop $pkgdir/etc/skel/.config/autostart/$_check.desktop
    install -Dm644 aur-warning.png $pkgdir/usr/share/icons/hicolor/40x40/status/aur-warning.png
}

