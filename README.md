## TWRP device tree for LG G6 (T-Mobile H872)

Add to `.repo/local_manifests/h872.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/lge/h872" name="android_device_lge_h872" remote="TeamWin" revision="android-6.0" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_h872-eng
make -j5 recoveryimage
```

Kernel sources are available at: https://github.com/jcadduono/android_kernel_lge_msm8996/tree/twrp-7.0
