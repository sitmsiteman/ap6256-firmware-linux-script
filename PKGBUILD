# Maintainer: Dan Johansen <strit@manjaro.org>

pkgname=ap6256-firmware
pkgver=2019.06
pkgrel=2
arch=('aarch64')
pkgdesc='Firmware files for the ap6256 wifi/bt module'
license=('unknown')
url="https://github.com/radxa/rk-rootfs-build"
source=('BCM4345C5.hcd'
        'fw_bcm43456c5_ag.bin'
        'fw_bcm43456c5_ag_apsta.bin'
        'fw_bcm43456c5_ag_p2p.bin'
        'nvram_ap6256.txt')
md5sums=('dc8b4466348c591174e96a31e4a1b13b'
         'ca63a118d10e69d0f84d8e06bbbe9d4f'
         'ca63a118d10e69d0f84d8e06bbbe9d4f'
         'ca63a118d10e69d0f84d8e06bbbe9d4f'
         '046a0d584bab0d2f774ba9f722a175f9')

package() {
    install -Dm755 "BCM4345C5.hcd" -t "${pkgdir}/usr/lib/firmware/"
    install -Dm755 "fw_bcm43456c5_ag.bin" -t "${pkgdir}/usr/lib/firmware/"
    install -Dm755 "fw_bcm43456c5_ag_apsta.bin" -t "${pkgdir}/usr/lib/firmware/"
    install -Dm755 "fw_bcm43456c5_ag_p2p.bin" -t "${pkgdir}/usr/lib/firmware/"
    install -Dm755 "nvram_ap6256.txt" -t "${pkgdir}/usr/lib/firmware/"
    # Wfi fix because of weird setup
    install -Dm755 "fw_bcm43456c5_ag.bin" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio.bin"
    install -Dm755 "nvram_ap6256.txt" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio.txt"
}
