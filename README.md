# Sambooca

Sambooca is a RootFS / Boot-Image builder for Single Board Computers. It works on Gentoo and utilizes Gentoo's Portage as the package manager. It provides it's own overlay to provide for neccesary changes and patches required to make certain software work on the target platform, as well as a rich set of profiles that do most of the configuration for you.

It's main aim is to provide a tool to create compact, down-to-the-essentials RootFS, tailored to the specific needs of each installation, while keeping the stuff out that makes Gentoo bulky - most notably the Portage tree, kernel sources, the package db and all build-time dependencies. It is rather easy to create a working X System far under 1G of space requirements.

While Sambooca systems basically -are- Gentoo, the things that make Gentoo seem unfit for embedded devices - in other words compiling, vast amounts of source code and a multitude of build dependencies and tools - remain on the managing PC. All compiling is done on your powerful workstation rather than on a rather slow and simple ARM device. To achieve that the target medium is mounted in a prefix location, either from a Boot image, the actual boot device, or (if supported) directly via USB Mass Storage support in "Management Mode". From there on you can manage your Sambooca system like you would any other Gentoo installation, and either put the boot device back into your SBC, or resume from management mode. 

Sambooca does not aim to nor has any ambitions to compete with out-of-the-box systems like Armbian. If you are looking for a linux distribution for you xPi that just works - Armbian is it. If you however looking for a way to tailor a highly optimized boot image for your hardware and needs - Sambooca is for you.

##

Supported SoCs

At first Sambooca aims to provide support for the multitude of Allwinner H3 devices, most notably from the OrangePi series. I also plan to support the Broadcom BCM2836 (RPi2), as well as the 64-bit SoCs Broadcom BCM2837 (RPi3) and Anlogic S905 (Odroid C2 and a couple of cheap TV boxes). But since the build process is modular there is little reason why other SBCs, even x86 ones, shouldn't work.
