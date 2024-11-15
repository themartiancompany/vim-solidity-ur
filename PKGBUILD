# SPDX-License-Identifier: AGPL-3.0
#
# Maintainer: Truocolo <truocolo@aol.com>
# Maintainer: Pellegrino Prevete (tallero) <pellegrinoprevete@gmail.com>

_proj="vim"
_pkg="solidity"
pkgname="${_proj}-${_pkg}"
pkgver=1.0
pkgrel=1
pkgdesc="Vim syntax file for Solidity."
arch=(
  'any'
)
_http="https://github.com"
_ns="tomlion"
url="${_http}/${_ns}/${pkgname}"
commit="569bbbedc3898236d5912fed0caf114936112ae4"
depends=(
  "${_proj}"
)
license=(
  "MIT"
)
source=(
  "${pkgname}::git+${url}#commit=${commit}"
)
sha256sums=(
  "SKIP"
)

package() {
  local \
    _dest \
    _files=()
  _files=(
    ftdetect
    ftplugin
    indent
    syntax
  )
  _dest="${pkgdir}/usr/share/vim/vimfiles"
  cd \
    "${pkgname}"
  install \
    -dm755 \
    "${_dest}"
  cp \
    -r \
    "${_files[@]}" \
    "${_dest}"
}
