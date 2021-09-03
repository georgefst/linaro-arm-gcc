# Maintainer: curlywei <dewei0724@gmail.com>

_target=arm-linux-gnueabihf
_pkgdate=2019.03
_compiler_name=gcc-arm

pkgname=${_target}-${_compiler_name}-bin
pkgver=8.3
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
sha512sums=('3578c32a9c0868d98264a1c9200b673aa89d9b97514322d40e175e079525f00beb2ca8efeb029656f9df7cfb2149715939c4097b2b3d2e3afa6ff6a4e91e0010')


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
