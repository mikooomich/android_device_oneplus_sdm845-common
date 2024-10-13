# Hi. Welcome to my playground.

Here is my personal device trees for enchilada (OnePlus 6). 
Fajita (Oneplus 6t) is *probably* supported with this common device repo, however I have done absolutely zero testing in that regard.

## Builds
You're probably better off installing Official LineageOS build, however, I have provided compiled builds in the [releases section](https://github.com/mikooomich/android_device_oneplus_sdm845-common/releases) should you wish to install them for whatever reason.. **These will be provided on an as-is bases with absolutely zero warranty.** 

Main changes from LineageOS
- Select cherry-picks from CrDroid
- [Per app volume](https://review.lineageos.org/q/per-app-volume)
- libperfmgr with my attempts to *hopefully* save battery
- Quick settings 4 rows, 3 columns, thinner brightness slider
- [KernelSU](https://kernelsu.org/)
- Signed with my own keys
    - Requires formatting data (factory reset) if you are coming from official LineageOS


## Building

Follow LineageOS instructions, and subsitiute repos. You will likely need the following
- [Kernel repo](https://github.com/mikooomich/crdroid_kernel_oneplus_sdm845)
- [Device repo](https://github.com/mikooomich/android_device_oneplus_enchilada)


Branch information
- lineage-21: The main "stable" branch
- lineage-21-staging: experimental changes
- staging/next: Very experimental changes


For libperfmgr, you will need the following additional requirements:
- [proprietary_vendor_oneplus_sdm845-common](https://github.com/mikooomich/proprietary_vendor_oneplus_sdm845-common)
- (Optional) [android_hardware_lineage_interfaces](https://github.com/mikooomich/android_hardware_lineage_interfaces/tree/libperf-power-saver) patches for disabling most hints in power saver mode 
