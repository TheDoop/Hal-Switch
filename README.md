# Hal-Swtich
`git clone https://github.com/TheDoop/Hal-Switch device/xiaomi/daisy/XiaomiParts`
`wget https://raw.githubusercontent.com/TogoFire/dt_xiaomi_daisy/xq/rootdir/etc/init.camera.sh /rootdir/etc/init.camera.sh`
`wget https://raw.githubusercontent.com/TogoFire/dt_xiaomi_daisy/xq/rootdir/etc/init.camera.rc /rootdir/etc/init.camera.rc`

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
