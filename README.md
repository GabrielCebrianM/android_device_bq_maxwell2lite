Slim device configuration for the bq Maxwell 2 Lite.

How to Build
---------------

Initialise from Slim:

    repo init -u git://github.com/SlimRoms/platform_manifest.git -b kk4.4

Use the following local manifest:

    <?xml version="1.0" encoding="UTF-8"?>
    <manifest>
      <remove-project name="SlimRoms/frameworks_av" />
      <remove-project name="SlimRoms/frameworks_native" />
      <project name="GabrielCebrianM/android_frameworks_av" remote="github" path="frameworks/av" revision="cm-11.0" />
      <project name="GabrielCebrianM/android_frameworks_native" remote="github" path="frameworks/native" revision="cm-11.0" />
      <project name="GabrielCebrianM/android_device_bq_maxwell2lite" remote="github" path="device/bq/maxwell2lite" revision="kk4.4" />
      <project name="GabrielCebrianM/android_device_bq_rockchip-common" remote="github" path="device/bq/rockchip-common" revision="kk4.4" />
      <project name="GabrielCebrianM/android_kernel_bq_maxwell2" remote="github" path="kernel/bq/maxwell2lite" revision="cm-11.0" />
      <project name="GabrielCebrianM/proprietary_vendor_bq" remote="github" path="vendor/bq" revision="cm-11.0" />
    </manifest>

Sync and build:

    repo sync -j4
    . build/envsetup.sh
    lunch full_maxwell2lite-userdebug

