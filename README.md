### Sonoma EFI Opencore 

I have been try for 5days to learn about efi opencore and how to hackintosh any PC

Just to realize that it can be easy and difficult at same time, especially coming from a background of windows where everything is already sat up

In the repo I have save my EFI with all necessary setting for a fully working Hackintosh with Sonoma, (worked also for Ventura)

## Issue I encoutered

[fixed] CPU compatibility, and getting error of not booting the OS it self
[fixed] Audio not working
    - by adding PciRoot(0x0)/Pci(0x1F,0x3):
        - device-id: 0x10028010
        - ig-platform-id: 0x887
    - or maybe adding VoodooHDA.kext, or AppleHDA.kext
[fixed] HD530 Graphic acceleration
    - this one took me alot, and it was tricky, I had to set in BIOS the graphic memory to be 64mb
    - disable VT-d
    - and one of repo that helped me fixig that was [repo](https://github.com/TECHNIKVERBOT/Dell-Precision-7520-OpenCore)
    - in boot-args: `-v keepsyms=1 debug=0x100 -igfxsklaskbl -cdfon igfxonln=1 hda-gfx`
[NotAchieved] Connecting dGPU Rx480, 
    - tried all opencore docs for this, only thing I got is a Flickering BlackScreen after boot
    - I heard about patching but I haven't tried it yet

[Fixed] Wireless mouse not working
    - by adding USBInjectAll.kext



## Tools used
- opencore configurator: (MacOS)
- ProperTree: (Windows)
- Opencore Auxilary Tool: (Windows)
- GenSMBIOS: (Windows)
- MountEFI: (MacOS)
- expolorer++: (Windows)
- Minitoll partition: (Windows)
- Clover Configurator: (MacOS)

## Useful links
- https://github.com/TECHNIKVERBOT/Dell-Precision-7520-OpenCore 
- https://github.com/zmlu/Hackintosh-OC-Colorful-C.B150M-i5-6500-Skylake-HD530
- 

## Verdict

It was a nice headhake for these late 5days, but I had to do that So I can have MacOS under my belt for future work, especially with React Native, and XCode
and I will aim to build a suitable hackintosh, with dual monitor
