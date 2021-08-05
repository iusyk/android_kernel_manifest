**Building Linux kernel with modules:**

Mandatory options to export:

Depending on your HW `TARGET_BOARD_PLATFORM=r8a779[5,6]`

`BUILD_CONFIG=common/build.config.xenvm`


Optional options:

`SKIP_DEFCONFIG=1` - skip defconfig stage

`SKIP_MRPROPER=1` - skip mrproper stage

```
repo init -u https://github.com/xen-troops/android_kernel_manifest -b common-android13-5.10-cr7-master -g all
repo sync -c
./build/build.sh
```

Built products could be found at `out/android13-5.10/dist`
