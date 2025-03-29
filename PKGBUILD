# Maintainer: Calliope System <calliopesystem@gmail.com>

pkgname=devede-git
_pkgname=devedeng
pkgver=4.20.0.r2.4143d9dd
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
optdepends=(
  'mplayer'
  'mpv'
  'vlc'
  'brasero'
  'k3b'
  'xfburn'
)
source=("git+https://gitlab.com/rastersoft/$_pkgname.git")
b2sums=('SKIP')

pkgver() {
  cd "$srcdir/$_pkgname"
  tag=$(git describe --tags --abbrev=0)
  rev=$(git rev-list --count "${tag}..HEAD")
  commit=$(git rev-parse --short=8 HEAD)
  echo "${tag}.r${rev}.${commit}"
}

prepare() {
  cd $_pkgname
  pkgver=$(pkgver)
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
