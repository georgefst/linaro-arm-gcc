# Maintainer: curlywei <dewei0724@gmail.com>

_target=arm-none-linux-gnueabihf
_pkgdate=2021.07
_compiler_name=gcc-arm

pkgname=${_target}-${_compiler_name}-bin
pkgver=10.3
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
sha512sums=('f161c7eeb58a3c6989093ab0a1ba5377464e47eae87aacb6289748ad323595b9bb76e96386305b0f0561545a6f14d4d15af0e90c2d0e993952a62f12746b6fd1')


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
