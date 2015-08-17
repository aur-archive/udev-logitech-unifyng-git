# Maintainer: Diego <cdprincipe@at@gmail@dot@com>

pkgname=udev-logitech-unifyng-git
pkgver=0.9.0
pkgrel=1
pkgdesc="udev rules for Logitech Unifyng and Nano receivers"
url="http://pwr.github.com/Solaar/"
license=('GPL2')
groups=()
arch=('any')
depends=()
options=(!emptydirs)
install=udev-logitech.install
source=("https://raw.github.com/pwr/Solaar/master/rules.d/42-logitech-unify-permissions.rules" 
        "https://raw.github.com/pwr/Solaar/master/lib/solaar/__init__.py"
        'udev-logitech.install')
md5sums=('SKIP'
         'SKIP'
         '285bc14d39cacfc9e6402834e4cc39d2')

pkgver() {
  echo $(cat "$srcdir/__init__.py" | grep -o '[0-9].*[0-9]')
}


package() {
  cd $srcdir
  install -D -m0644 42-logitech-unify-permissions.rules "$pkgdir/etc/udev/rules.d/42-logitech-unify-permissions.rules"
}
