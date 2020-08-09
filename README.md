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

Add `Android.mk` :
```
include $(CLEAR_VARS)
LOCAL_MODULE       := init.camera.rc
LOCAL_MODULE_TAGS  := optional
LOCAL_MODULE_CLASS := ETC
LOCAL_SRC_FILES    := etc/init.camera.rc
LOCAL_MODULE_PATH  := $(TARGET_OUT_VENDOR_ETC)/init/hw
include $(BUILD_PREBUILT)

include $(CLEAR_VARS)
LOCAL_MODULE       := init.camera.sh
LOCAL_MODULE_TAGS  := optional
LOCAL_MODULE_CLASS := ETC
LOCAL_SRC_FILES    := etc/init.camera.sh
LOCAL_MODULE_PATH  := $(TARGET_OUT_VENDOR_EXECUTABLES)
include $(BUILD_PREBUILT)
```
add `device/xiaomi/daisy/rootdir/init.qcom.rc` :
```
import /vendor/etc/init/hw/init.camera.rc
```
