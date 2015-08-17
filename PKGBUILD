# Maintainer: Jakub Klinkovský <j.l.k@gmx.com>

pkgname=python2-scandir-git
pkgdesc="scandir, a better directory iterator that returns all file info OS provides. (python2 version)"
pkgver=39.965aac8
pkgrel=1
arch=('i686' 'x86_64')
url="https://github.com/benhoyt/scandir"
license=('BSD')
depends=('python2')
makedepends=('git')
source=('git://github.com/benhoyt/scandir.git')
md5sums=('SKIP')

_gitname=scandir

pkgver() {
  cd "$_gitname"
  echo "$(git rev-list --count HEAD).$(git describe --always )"
}

build() {
  cd "$_gitname"
  python2 setup.py build
}

package() {
  cd "$_gitname"
  python2 setup.py install --prefix=/usr --root="$pkgdir" --optimize 1
}

# vim:set ts=2 sw=2 et:
