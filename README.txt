audio_hdmi_uefi
============
OS X UEFI AMD/Nvidia/HD4K/HD3K HDMI Audio dsdt edits

This guide enables OS X HDMI audio on Intel based motherboards with a bootable clean install of OS X.  Supported HDMI audio graphics systems are AMD discrete graphics cards (HD5xxx and HD6xxx), Nvidia discrete graphics cards (4xx, 5xxx and 6xx) and Intel HD4K and HD3K integrated graphics systems.  The Optimized AppleHDA.kext supports HDMI audio and Realtek audio codecs (ALC885, ALC887, ALC888, ALC889, ALC892 and ALC898) for onboard audio.  The native ML AppleHDA.kext supports only HDMI audio when configured properly. In Mountain Lion, the Optimized AppleHDA.kext supports 2 Audio_IDs for HDMI and Realtek onboard audio:
1. Audio_ID: 1 supports AMD/Nvidia HDMI and 3, 5 and 6 port ALC8xx onboard audio (HD3000/       HD4000 HDMI audio not available)
2. Audio_ID: 3 supports HD3000/HD4000 with or without AMD/Nvidia HDMI and 3, 5 and 6 port ALC8xx onboard audio (Black port - not available)

Notes
1. Native ML AppleHDA.kext, use Audio_ID: 1, for HDMI audio only/no onboard audio
2. Both Integrated and Discrete HDMI audio, use Audio_ID:3, for HDMI audio and supported Realtek on board audio
3. Framebuffer edits may be required in addition to dsdt edits for working HDMI audio

More Information
1. Mountain Lion: Optimized AppleHDA for Realtek ALC8xx
http://www.tonymacx86.com/audio/76202-mountain-lion-optimized-applehda-realtek-alc8xx.html#post472375
2. ML: UEFI HDMI Audio
http://www.tonymacx86.com/hdmi-audio/100492-easy-guide-ml-uefi-hdmi-audio.html
3. Mountain Lion HDMI Audio
http://www.tonymacx86.com/hdmi-audio/70765-mountain-lion-hdmi-audio.html

ML: UEFI HDMI Audio dsdt edits
1. MaciASL - http://sourceforge.net/projects/maciasl/?source=navbar
2. Configuration: MaciASL/Preferences/Sources/+/
3. URL: https://raw.github.com/toleda/audio_uefi/master
4. Download/ZIP: https://github.com/toleda/audio_hdmi_uefi

Usage
1. If no dsdt; extract dsdt, MaciASL/File/New from ACPI/DSDT
2. MaciASL/File/Open dsdt
3. MaciASL/Patch/toleda_hdmi_uefi/Select Patch
4. MaciASL/Patch/Apply (Repeat, as necessary) 
5. MaciASL/Patch/Close
6. MaciASL/Compile
7. MaciASL/File/Save As…/ACPI Machine Language Binary/dsdt.aml

Installation - edited dsdt.aml to Extra
1. MaciASL/File/Save As…/ACPI Machine Language Binary/Extra/dsdt.aml (add extension)

Guides
1. OS X UEFI AMD/Nvidia/HD4K/HD3K HDMI Audio
1a. [Guide] ML-uefi_hdmi_audio_dsdt_edits
1b. Patches
    ib1. UEFI-Clean Compile - fix native dsdt compiler errors for successful dsdt edits
    uefi1. Desktop-AMD/Nvidia-A1 - AMD/Nvidia HDMI audio dsdt edits
    uefi2. Desktop-HD4K/HD3K/AMD/Nvidia-A3 - HD4000 HDMI audio dsdt edits
    uefi3. Laptop-A3-FB_01 - Laptop HD4K/HD3K HDMI audio dsdt edits
    uefi4. Laptop-A3-FB_03 - Laptop HD4K/HD3K HDMI audio dsdt edits
    uefi5. NUC-HD4K-A1 - NUC HDMI audio edits (2xHDMI and TB)
    ib4. HD4K-on-6_Series_MEI - HD4K MEI dsdt edit (apply once, only with uefi1 - uefi4)
    3b5. HD3K-on-7_Series_MEI - HD3K MEI dsdt edit (apply once, only with uefi1 - uefi4)

Troubleshooting/Post
1. http://www.tonymacx86.com/hdmi-audio/100492-easy-guide-ml-uefi-hdmi-audio.html
2. http://www.insanelymac.com/forum/topic/291103-mountain-lion-hdmi-audio/

toleda
https://github.com/toleda/audio_hdmi_uefi
Patches
README.txt