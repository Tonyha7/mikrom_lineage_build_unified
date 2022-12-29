
## Building PHH-based MikRom LineageOS GSIs ##



��л����[Ǩ�Ƶ���׿12.1](https://github.com/dqzg12300/MikRom/issues/40#issuecomment-1364508642)

׼������:
����300G�ռ�
16G�����ڴ棨��24G��
ͨ�������绷��

~~~
git clone https://github.com/akhilnarang/scripts
./scripts/setup/android_build_env.sh
~~~

First, open a new Terminal window, which defaults to your home directory. Create a new working directory for your LineageOS build and navigate to it:

    mkdir lineage-19.x-build-gsi; cd lineage-19.x-build-gsi

Initialize your LineageOS workspace:

    repo init -u https://github.com/LineageOS/android.git -b lineage-19.1

Clone both this and the patches repos:

    git clone https://github.com/Tonyha7/mikrom_lineage_build_unified lineage_build_unified -b lineage-19.1
    git clone https://github.com/Tonyha7/lineage_patches_unified lineage_patches_unified -b lineage-19.1

Finally, start the build script - for example, to build for all supported archs:

    bash lineage_build_unified/buildbot_unified.sh treble 64VN 64VS 64GN

Be sure to update the cloned repos from time to time!

---

Note: VNDKLite and Secure targets are generated from built images instead of source-built - refer to [sas-creator](https://github.com/AndyCGYan/sas-creator).

---

This script is also used to make device-specific and/or personal builds. To do so, understand the script, and try the `device` and `personal` keywords.

