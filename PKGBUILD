# Maintainer: Dawid Marcin Grzesiak <230375+dmgr@users.noreply.github.com>
# Hooks: https://www.reddit.com/r/archlinux/comments/4zrsc3/keep_your_system_fully_functional_after_a_kernel/d6yin0r/
pkgname=kernel-modules-hook-dmg
pkgver=0.1.8
pkgrel=1
pkgdesc="Keeps your system fully functional after a kernel upgrade (optimized with hardlinks)"
arch=('any')
url="https://github.com/saber-nyan/kernel-modules-hook"
license=('UNLICENSE')
provides=('kernel-modules-hook')
conflicts=('kernel-modules-hook')
install="kernel-modules-hook.install"
source=(
  linux-modules-cleanup.conf
  linux-modules-cleanup.service
  10-linux-modules-post.hook
  10-linux-modules-pre.hook
  UNLICENSE
)
sha256sums=(SKIP SKIP SKIP SKIP SKIP)

package() {
  install -Dm644 linux-modules-cleanup.conf "$pkgdir/usr/lib/tmpfiles.d/linux-modules-cleanup.conf"
  install -Dm644 linux-modules-cleanup.service "$pkgdir/usr/lib/systemd/system/linux-modules-cleanup.service"
  install -Dm644 10-linux-modules-post.hook "$pkgdir/usr/share/libalpm/hooks/10-linux-modules-post.hook"
  install -Dm644 10-linux-modules-pre.hook "$pkgdir/usr/share/libalpm/hooks/10-linux-modules-pre.hook"
  install -Dm644 UNLICENSE "$pkgdir/usr/share/licenses/$pkgname/UNLICENSE"
}
