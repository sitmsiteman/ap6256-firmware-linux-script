# Maintainer: Dan Johansen <strit@manjaro.org>

pkgname=ap6256-firmware
pkgver=2019.08
pkgrel=1
arch=('aarch64')
pkgdesc='Firmware files for the ap6256 wifi/bt module'
license=('unknown')
url="https://github.com/radxa/rk-rootfs-build"
source=('BCM4345C5.hcd'
        'fw_bcm43456c5_ag.bin'
        'nvram_ap6256.txt')
md5sums=('4017a2bda950875f1fb3132b9ba7bbba'
         '4df335e66e8dedb9701c79bbee092e25'
         '259228920fb6c7e9369fdd13e7be1b43')

package() {
    install -Dm755 "BCM4345C5.hcd" -t "${pkgdir}/usr/lib/firmware/"
    install -Dm755 "BCM4345C5.hcd" "${pkgdir}/usr/lib/firmware/brcm/BCM.hcd"
    install -Dm755 "fw_bcm43456c5_ag.bin" -t "${pkgdir}/usr/lib/firmware/fw_bcm43456c5_ag.bin"
    install -Dm755 "fw_bcm43456c5_ag.bin" -t "${pkgdir}/usr/lib/firmware/fw_bcm43456c5_ag_apsta.bin"
    install -Dm755 "fw_bcm43456c5_ag.bin" -t "${pkgdir}/usr/lib/firmware/fw_bcm43456c5_ag_p2p.bin"
    install -Dm755 "nvram_ap6256.txt" -t "${pkgdir}/usr/lib/firmware/"
    # Wfi fix because of weird setup
    install -Dm755 "fw_bcm43456c5_ag.bin" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio.bin"
    install -Dm755 "nvram_ap6256.txt" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio.txt"
    install -Dm755 "nvram_ap6256.txt" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio.radxa,rockpi4.txt"
}
