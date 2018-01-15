## TWRP device tree for OnePlus 3 (oneplus3)

Add to `.repo/local_manifests/oneplus3.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/oneplus/oneplus3" name="oneplus3" remote="TeamWin" revision="android-8.0" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
make clean
. build/envsetup.sh
lunch omni_oneplus3-userdebug
make recoveryimage -j16
```

Kernel sources are available at: https://github.com/jcadduono/android_kernel_oneplus_msm8996/tree/3-twrp-8.0
