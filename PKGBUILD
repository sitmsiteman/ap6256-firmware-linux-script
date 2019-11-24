# Maintainer: Dan Johansen <strit@manjaro.org>

pkgname=ap6256-firmware
pkgver=2019.11
pkgrel=2
arch=('aarch64')
pkgdesc='Firmware files for the ap6256 wifi/bt module'
license=('unknown')
url="https://github.com/radxa/rk-rootfs-build"
conflicts=('ap6398s-firmware')
source=('BCM4345C5.hcd'
        'fw_bcm43456c5_ag.bin'
        'nvram_ap6256.txt')
md5sums=('4017a2bda950875f1fb3132b9ba7bbba'
         '4df335e66e8dedb9701c79bbee092e25'
         '259228920fb6c7e9369fdd13e7be1b43')

package() {
    install -Dm644 "BCM4345C5.hcd" -t "${pkgdir}/usr/lib/firmware/"
    install -Dm644 "BCM4345C5.hcd" "${pkgdir}/usr/lib/firmware/brcm/BCM.hcd"
    install -Dm644 "BCM4345C5.hcd" -t "${pkgdir}/usr/lib/firmware/brcm/"
    install -Dm644 "nvram_ap6256.txt" -t "${pkgdir}/usr/lib/firmware/"
    #install -Dm644 "nvram_ap6256.txt" -t "${pkgdir}/usr/lib/firmware/brcm/"
    # Wfi fix because of weird setup
    install -Dm644 "fw_bcm43456c5_ag.bin" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio.bin"
    #install -Dm644 "fw_bcm43456c5_ag.bin" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio_apsta.bin"
    #install -Dm644 "fw_bcm43456c5_ag.bin" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio_p2p.bin"
    install -Dm644 "nvram_ap6256.txt" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio.radxa,rockpi4.txt"
    install -Dm644 "nvram_ap6256.txt" "${pkgdir}/usr/lib/firmware/brcm/brcmfmac43456-sdio.pine64,pinebook-pro.txt"
}
