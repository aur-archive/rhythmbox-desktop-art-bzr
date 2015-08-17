# Contributor: kaivalagi <m_buck@hotmail.com>

pkgname=rhythmbox-desktop-art-bzr
pkgver=2
pkgrel=1
pkgdesc="Provides Rhythmbox controls, song info and cover art on the desktop."
arch=('i686' 'x86_64')
url="https://code.launchpad.net/~conky-companions/+junk/rhythmbox-desktop-art"
license=('GPL3')
depends=('rhythmbox')
makedepends=('bzr')
source=()
md5sums=()
_bzrbranch=lp:~conky-companions/+junk
_bzrmod=rhythmbox-desktop-art
_targetfolder=usr/lib/rhythmbox/plugins/desktop-art

build() {
  cd $startdir/src
  msg "Connecting to the server...."
    
  bzr branch $_bzrbranch/$_bzrmod -q -r $pkgver

  msg "BZR checkout done or server timeout"
  msg "Starting install..."

  mkdir -p $startdir/pkg/${_targetfolder}
  msg "Copying *.py..."
  cp $startdir/src/rhythmbox-desktop-art/*.py $startdir/pkg/${_targetfolder}
  msg "Copying *.glade..."
  cp $startdir/src/rhythmbox-desktop-art/*.glade $startdir/pkg/${_targetfolder}
  msg "Copying *.rb-plugin..."
  cp $startdir/src/rhythmbox-desktop-art/*.rb-plugin $startdir/pkg/${_targetfolder}

  #install -m 644 $startdir/src/rhythmbox-desktop-art/* $startdir/pkg/${_targetfolder}
}

package() {
  return 0
}

