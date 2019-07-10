#PEMU
a qemu built for fuchsiaOS. This idea has been on our minds for many weeks. And I'm going to finally start it. PEMU will have a flutter
based interface to choose ISO's and make disk images to install your os to. And that means you could run debain linux inside fuchsiaOS.


## Getting Started
1. first you want to clone prickle. `git clone https://github.com/dahlia-os/prickle-emulator.git`

2. then... cd into the qemu folder. `cd prickle-emulator/lib/qemu`

3. then you can install ubuntu. `sh install-ubuntu.sh`

4. when ubuntu is finished you can boot it up. Exit out of the ubuntu install UI (when it's done) and boot up ubuntu. `sh run-ubuntu.sh`

## Notes (IMPORTENT)
there have been reports of this not working properly in deepin which is built on debian... Noah Cain and I will test cloning this on other
devices with ubuntu to check if it works properly. If it doesn't work for you please make an issue and I will have a look on what I can do.

## Architectures
at the moment this only has support for qemu-system-x86_64. which is located in 
`/home/ender/Dahlia/prickle-emulator/lib/qemu/x86_64-softmmu/qemu-system-x86_64`

to run it you must use `./qemu-system-x86_64 -(perimeters)`

## Ram, KVM, CPU's Oh My
I think most of the people are better at using QEMU than me. To configure qemu when ubuntu boots edit `run-ubuntu.sh` it should look like
this `./x86_64-softmmu/qemu-system-x86_64 -hda ubuntu.img -m 2.5G -boot d` -m = memory the default is 2.5GB of ram. It shouldn't slow your computer down unless your using KDE or MATE, I recommend using lxde. Be sure to set the CPU and the MACHINE. if your still not sure on how
to use QEMU then check out some of these links that will give you some ideas. And make sure you have access to /dev/kvm if you want to use KVM.

: https://wiki.qemu.org/Documentation

: https://wiki.gentoo.org/wiki/QEMU/Options



