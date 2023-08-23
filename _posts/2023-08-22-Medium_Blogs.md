---
title: "How to solve Kernel panic- not syncing : IO-APIC + timer doesnt work"
date: 2023-08-22
categories: [Blogging,Tutorial]
---

## How to solve Kernel panic- not syncing : IO-APIC + timer doesnt work?

Hey hackers, today i want to show you how to solve " Kernel panic - not syncing: IO-APIC + timer doesn't work? Boot with apic-debug and send a report. Then try booting with the 'noapic' option. This is solution by user named "VM_Novice22".  
![Kernel Panic error](/assets/images/first_image.webp)
_Kernel Panic error_
when i was trying to install metasploitable2 in my virtual. I was constantly facing this error. To solve this, i was manually setting noapic in boot options. After every restart i need to do that again. I came through a virtual box forum page when i was searching for a permanent solution.  
The solution is given by a user named "VM_Novice22". The credit goes to him. Now lets solve this error. Go to your virtual box root directory, mine is located in "C:\Program Files\Oracle\VirtualBox". Your directory is different than mine. Open powershell terminal in this directory.  
Type the following commands one by one. The first command is ".\VBoxManage modifyvm <uuid|vmname> - acpi off" replace "<uuid|vmname>" with your VM name, mine is Metasploitable.  
![Picture](/assets/images/second_image.webp)
_Executing command in powershell_  
there are no errors, we are in the right path. we will now execute next command ".\VBoxManage modifyvm <uuid|vmname> - ioapic off" replace "<uuid|vmname>" with your VM name, mine is Metasploitable.  
![Picture](/assets/images/third_image.webp)
_Executing command in powershell_  
Finally we need to open metasploitable in virtualbox and enter "msfadmin" as username and password.
![Picture](/assets/images/fourth_image.webp)
_We solved the error_  
Happy hacking………………………….
