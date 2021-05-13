# TWRP Device Tree for Walton Primo NX3 Plus for building TWRP Touch recovery 

NX3 Plus Specification:
Brand: Walton
Model: Primo NX3+
Device Type – Android Smartphone
CPU- Octa-Core 1.3 GHz ARM Cortex-A53
Chipset: MediaTek MT6753
Camera – 13 Megapixel With LED Flash | 8 Megapixel Front camera
Memory :RAM-3GB | ROM 16GB  External Memory Storage up to 128GB
Display – Screen size 5.5 inches AMOLED HD
Dimension & Weight – 155 mm x 76.4 mm x 7.4 mm, 153g
Battery –Non-Removable Lithium-Polymer 3,150 mAh battery
Dual (Micro + Micro) SIM Smartphone
support 2G/3G/4G Networks with a data speed of Download Up to 21 Mbps, Upload Up to 5.76 Mbps in 3G and LTE Cat4 150 / 50 Mbps in 4G networks.
Sensors: Proximity Sensor, Accelerometer, Compass, Ambient Light, Hall
Color:Gold and Blue
Operating System: Android 5.1.1 Lollipop
Price : ~ $230 (INR 14,000 ) Approx
More Feature – Comes with Rounded Edges, Dual Sim with Dual Standby DTS Sound System, Voice Search Support, Type-C USB, 65 Megapixels Camera with Ultra-Pixel Mode.

# it's time to build a TWRP recovery image
Clone minimal TWRP environment
Follow the instruction in this page
https://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni

Remember to clone the correct version of TWRP based on what Android version your phone have! If your phone have Android 8.0, clone twrp-8.0 branch

Move device tree to TWRP sources
Copy working/(brand)/(device) folder to device/(brand)/(device) folder in TWRP sources
Example:

brand name: walton
device codename: NX3+
Copy working/walton/NX3+ to device/walton/NX3+ in TWRP sources
Building
Open a terminal with the current dir pointing to TWRP sources root
Then type
. build/envsetup.sh
to initialize the environment

After that, type
lunch omni_codename-eng
where codename is the codename of your phone

If that is successful, type
mka recoveryimage
to build the recovery

If also that is successful, congratulation!
Go to out/target/product/codename/ (codename is your device codename) and you will find your recovery.img
