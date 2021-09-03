# Maintainer: curlywei <dewei0724@gmail.com>

_target=arm-none-linux-gnueabihf
_pkgdate=2019.12
_compiler_name=gcc-arm

pkgname=${_target}-${_compiler_name}-bin
pkgver=9.2
pkgrel=0
pkgdesc="The GNU Compiler Collection- cross compiler for ARMv7 EABI hard float target. (Linaro)"
arch=('x86_64')
url="https://developer.arm.com/-/media/Files/downloads/gnu-a"
license=('GPL' 'LGPL')
groups=(${_target}-toolchain-linaro-bin)
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=("${_target}-gcc")
replaces=("${_target}-gcc")
backup=()
options=(!emptydirs !strip staticlibs)
install=
changelog=
source=(${url}/${pkgver}-${_pkgdate}/binrel/${_compiler_name}-${pkgver}-${_pkgdate}-${arch}-${_target}.tar.xz)
sha512sums=('93f3486dad9d330b658bf75b70a54e7071a707ebbc0026531fab9d51d79e552e3159fe8f0e5434d0c4735a2df592d6c36d0fccd7846eb4240d2ecc39e5391d8d')


package() {
	mkdir -p ${pkgdir}/usr
	cp -a ${srcdir}/${_compiler_name}-${pkgver}-${_pkgdate}-${arch}-${_target}/* ${pkgdir}/usr

	rm -f 	${pkgdir}/usr/*-manifest.txt
	rm -f 	${pkgdir}/usr/bin/runtest
	rm -f 	${pkgdir}/usr/lib/lib*
	rm -rf 	${pkgdir}/usr/include
	rm -rf 	${pkgdir}/usr/lib/bfd-plugins/libdep.so
	rm -rf 	${pkgdir}/usr/lib64/lib*
	rm -rf 	${pkgdir}/usr/share/{dejagnu,doc,gcc-*,gdb,info,locale}
	rm -rf 	${pkgdir}/usr/share/man/{man1/runtest.1,man5,man7}
}
