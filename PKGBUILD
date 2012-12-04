# Maintainer: François-Xavier Thomas <fx.thomas+arch@gmail.com>
pkgname=android-automount
pkgver=0.1
pkgrel=1
pkgdesc="Adds udev rules to automount Android devices"
arch=('any')
url="https://github.com/fxthomas/android-automount"
license=('unknown')
depends=(go-mtpfs-git daemonize)
source=('99-android-mtp.rules' 'android-mtp@.service' 'mtp')
md5sums=('f1976d53148cdf6a914544a9848d5d56'
         '98ad3d341ad4425abfee7fd949e4da63'
         '225253503daca8c75ef2dbc3bd25db69')
install='android-automount.install'

package() {
  mkdir -p $pkgdir/usr/lib/udev/rules.d/
  mkdir -p $pkgdir/usr/lib/systemd/system/
  mkdir -p $pkgdir/usr/bin/
  cp $srcdir/99-android-mtp.rules $pkgdir/usr/lib/udev/rules.d/99-android-mtp.rules
  cp $srcdir/android-mtp@.service $pkgdir/usr/lib/systemd/system/android-mtp@.service
  cp mtp $pkgdir/usr/bin/mtp
  chmod a+r $pkgdir/usr/lib/udev/rules.d/99-android-mtp.rules
  chmod a+r $pkgdir/usr/lib/systemd/system/android-mtp@.service
  chmod a+rx $pkgdir/usr/bin/mtp
}

# vim:set ts=2 sw=2 et:
