# ap6256-firmware-linux-script

Shell script for installing pinebook pro bluetooth/wifi (brcmfmac43456) firmware on linux.

Firmware files are taken directly from manjaro-arm gitlab.

## Troubleshooting

If you can't connect to a WPA2-PSK encrypted network, you might need to tweak the kernel module options for brcmfmac.

Check the `brcmfmac.conf` file and copy it to `/etc/modprobe.d/`

## Reactivate WiFi Module

To restart the WiFi driver after re-enabling WiFi using the Privacy Switch (Pine + F11), run the command below:

```
sudo tee /sys/bus/platform/drivers/dwmmc_rockchip/{un,}bind <<< "$(basename /sys/devices/platform/fe310*)"
```
