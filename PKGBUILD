# Maintainer: Balló György <ballogyor+arch at gmail dot com>
# Contributor: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Andrea Scarpino <andrea@archlinux.org>
# Contributor: Javier 'Phrodo_00' Aravena <phrodo.00@gmail.com>
# Contributor: Daniel J Griffiths <ghost1227@archlinux.us>

pkgname=devede-git
_pkgname=devedeng
pkgver=4.19.0
pkgrel=1
pkgdesc='Program to create Video DVDs and CDs'
arch=('any')
url='https://rastersoft.com/programas/devede.html'
license=('GPL-3.0-only')
depends=(
  'cdrtools'
  'dvdauthor'
  'ffmpeg'
  'gdk-pixbuf2'
  'glib2'
  'gtk3'
  'hicolor-icon-theme'
  'python'
  'python-cairo'
  'python-gobject'
  'python-setuptools'
  'vcdimager'
)
makedepends=(
  'git'
  'python-build'
  'python-installer'
  'python-setuptools-gettext'
  'python-wheel'
)
source=("git+https://gitlab.com/CalliopeSystem/$_pkgname.git")
b2sums=('SKIP')

prepare() {
  cd $_pkgname
  sed -i "/share', 'pixmaps/d;s|/usr', 'share|share|" setup.py
}

build() {
  cd $_pkgname
  python -m build --wheel --no-isolation
}

package() {
  cd $_pkgname
  python -m installer --destdir="$pkgdir" dist/*.whl
}
