
pkgname=firmware-tenor-g
pkgver=5
pkgrel=0
pkgdesc="Firmware for Tenor G"
url="https://github.com/Kiciuk/proprietary_firmware_tenorg"
arch="aarch64"
license="proprietary"
options="!check !strip !archcheck"
_commit="d03e9e67c357fe241e8cbee47034ca634e882d65"
source="https://github.com/Kiciuk/proprietary_firmware_tenorg/archive/$_commit.zip"
builddir="$srcdir/proprietary_firmware_tenorg-$_commit"

_fwdir="/lib/firmware/postmarketos"

package() {
	# parent package is empty
	mkdir -p "$pkgdir"

	# modem firmware
	install -Dm644 modem/mba.mbn -t "$pkgdir/$_fwdir"
	install -Dm644 modem/modem.* -t "$pkgdir/$_fwdir"

	# video firmware
	install -Dm644 apnhlos/venus.* -t "$pkgdir/$_fwdir"

	# WiFi/BT firmware
	install -Dm644 apnhlos/wcnss.* -t "$pkgdir/$_fwdir"
	install -Dm644 firmware/wlan/prima/WCNSS_qcom_wlan_nv.bin -t "$pkgdir/$_fwdir"/wlan/prima

	# ADSP firmware
	install -Dm644 modem/adsp.* -t "$pkgdir/$_fwdir"

	# GPU firmware
	install -Dm644 apnhlos/a506_zap.* -t "$pkgdir/$_fwdir"
}

