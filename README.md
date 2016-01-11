CyanogenMod 12.1 for SEMC 2011 devices
===============

Local manifest needed to build cm-12.1 for the Sony Ericsson 2011 phone line.

Instructions:
-------------

Initialize the CyanogenMod source repository

    repo init -u git://github.com/CyanogenMod/android.git -b cm-12.1

Get the required local manifest:

    mkdir -p ~/android/system/.repo/local_manifests
    curl https://raw.githubusercontent.com/niks255/local_manifests/cm-12.1/semc.xml > .repo/local_manifests/semc.xml

Sync up:

    repo sync

Download some commits from CyanogenMod gerrit which are not accepted yet

    ln -s vendor/extra/updates.sh updates.sh
./updates.sh

Now you can build a ROM. For example, to build for xperia pro, type in:

    . build/envsetup.sh
    breakfast iyokan
    brunch iyokan
