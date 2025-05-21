# Maintainer: Eyad Merajuddin(CanadianGamer) <easygamer2019@gmail.com>
pkgname=emos-installer
pkgver=1.0
pkgrel=1
pkgdesc="Graphical installer for EMOS Linux"
arch=('any')  # 'any' for scripts/arch-independent files
url="https://github.com/EM-OS/EMOS-INSTALLER"
license=('GPL3')
depends=('gum' 'bash' 'arch-install-scripts')  # List runtime dependencies
source=("git+$url.git")
sha256sums=('SKIP')  # Skip checksum for Git repos

package() {
  cd "$srcdir/EMOS-INSTALLER"
  install -Dm755 emos-installer.sh "$pkgdir/usr/local/bin/emos-installer"
  # Install additional files (e.g., docs, configs) if needed
}