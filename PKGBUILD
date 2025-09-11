pkgname=lext-artwork-lubuntu
pkgdesc="LXQt theme: Lubuntu-Arc (for Lubuntu $upstreampkgver)"           

# Intentionally not following the release and version numbering of Lubuntu
pkgver=1 
pkgrel=1

orgpkgname=lubuntu-artwork
upstreampkgver=25.10.2

arch=('any')                                                      
url="https://github.com/lext-next/lext-artwork-lubuntu"                 
license=('GPL')                                                          
depends=('lxqt-session')
conflicts=('lubuntu-artwork' 'lubuntu-artwork-18-04')
#source=("http://archive.ubuntu.com/ubuntu/pool/universe/l/${orgpkgname}/${orgpkgname}_${upstreampkgver}.tar.xz")
source=("https://github.com/lext-next/lext-artwork-lubuntu/blob/main/lubuntu-artwork_25.10.2.tar.xz")
                                                                                   
sha256sums=('SKIP')  # for testing; replace with real checksum later                 
                                                                                       
package() {
#   msg "Current srcdir is: $srcdir"
#   msg "Current pkgdir is: $pkgdir"
#   set -x
#   trap 'set +x' RETURN   # automatically disable tracing on function exit

    install -d "$pkgdir/usr/share/lxqt/themes"

#   cp -rv "$srcdir"/artwork/src/usr "$pkgdir"
    cp -r "$srcdir"/artwork/src/usr "$pkgdir"

    msg "*** READY ***"
}
