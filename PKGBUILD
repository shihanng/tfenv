# Maintainer: Jonatan Bravo <zephrax@gmail.com>
pkgname=tfenv
pkgver=0.6.0
pkgrel=1
epoch=
pkgdesc="Terraform version manager inspired by rbenv"
arch=("x86_64")
url="https://github.com/tfutils/tfenv"
license=('MIT')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=("tfenv")
source=("git://github.com/tfutils/tfenv.git")
md5sums=("SKIP")
validpgpkeys=()

package() {
	cd "${srcdir}/${pkgname}"
	mkdir -p "${pkgdir}/usr/local/bin"
	mkdir -p "${pkgdir}/usr/local/libexec"
	echo $srcdir
	ls -lah
	install -m755 "bin/${pkgname}" "${pkgdir}/usr/local/bin/${pkgname}"
	install -m755 "bin/terraform" "${pkgdir}/usr/local/bin/terraform"
	for i in `ls ${srcdir}/${pkgname}/libexec/`; do
		install -m755 "${srcdir}/${pkgname}/libexec/$i" "${pkgdir}/usr/local/libexec/$i"
	done
	chmod +x ${pkgdir}/usr/local/bin/${pkgname}
}
