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
                                
prepare() {

	# remove Debian install parts

	unwanted_stuff=(debian  Makefile  README.md)
	for stuff in "${unwanted_stuff[@]}"; do
		rm -R "$srcdir/artwork/$stuff"
	done

	# remove grub related stuff

	rm -R "$srcdir/artwork/src/etc"

	unwanted_aspects=(grub lubuntu Kvantum plymouth sddm)
	# lubuntu contains openbox-3 stuff and wallpapers
	for aspect in "${unwanted_aspects[@]}"; do
		rm -R "$srcdir/artwork/src/usr/share/$aspect"
	done

	ls -lRt $srcdir
}

package() {

	msg "*** now install -d... ***"

    install -d "$pkgdir/usr/share/lxqt/themes"

	msg "*** now cp -r... ***"

    cp -r "$srcdir"/artwork/src/usr "$pkgdir"

    msg "*** READY ***"
}
