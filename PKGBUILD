# Maintainer: Jan Kocka <kockahonza@gmail.com>
pkgname=dbus_filemanager
pkgver=1
pkgrel=1
pkgdesc="Simple, customizable python dbus daemon implementing FileManager1"
arch=(any)
url=""
license=("GPL")
depends=("python" "python-gobject" "python-dbus" "python-systemd" "python-pyxdg")
source=("org.${pkgname}.FileManager1.service" "${pkgname}.py")
sha256sums=('9f9a375145fa3e5092bb93e2c152084a4c2e7c97544156f99e3163ab5d838445'
            'e381a1f72c736cf897e3e6fd830514c3766a1ce9c9be97f8c088e539342b5436')


package() {
    mkdir -p "${pkgdir}/usr/bin"
    cp "${srcdir}/${pkgname}.py" "${pkgdir}/usr/bin/"
    chmod +x "${pkgdir}/usr/bin/${pkgname}.py"

    mkdir -p "${pkgdir}/usr/share/dbus-1/services"
    cp "${srcdir}/org.${pkgname}.FileManager1.service" "${pkgdir}/usr/share/dbus-1/services"
}
