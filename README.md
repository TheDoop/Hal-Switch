# Hal-Swtich
1. `git clone https://github.com/TheDoop/Hal-Switch device/xiaomi/daisy/XiaomiParts`
2. `curl https://raw.githubusercontent.com/TogoFire/dt_xiaomi_daisy/xq/rootdir/etc/init.camera.sh --output device/xiaomi/daisy/rootdir/etc/init.camera.sh`
3. `curl https://raw.githubusercontent.com/TogoFire/dt_xiaomi_daisy/xq/rootdir/etc/init.camera.rc --output device/xiaomi/daisy/rootdir/etc/init.camera.rc`

add device mk:
```
# XiaomiParts
PRODUCT_PACKAGES += \
    XiaomiParts
```
and:
```
PRODUCT_PACKAGES += \
    init.camera.rc \
    init.camera.sh
```
