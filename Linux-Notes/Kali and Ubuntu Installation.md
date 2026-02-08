# Linux Installation

I want to install Linux so that I can use Linux without the extra layer of WSL, giving me full utilization of the OS.

## Creating Partitions

For this installation I only had one 1TB hard drive to install on so I needed to make another partiotion. I went into Windows disk manager and right clicked on my (Z:) drive. Then I selected "Shrink Volume" and set the amount to shrink to 474747MB (exactly half of the existing partition) and the name to Ubuntu (X:). I also renamed the (Z:) partition to Kali.

## Rufus

Rufus is the flashing program I used for installing Kali and Ubuntu. The setup was very simple, all i had to do was download the app and run the file.

## Flashing

The flashing was also very simple, all I had to do was download the ISO and flash with Rufus.

## Installation

The first thing to do when installing an OS is to restart the computer and boot into BIOS. Then select the flashed drive to boot.

### Kali

The Kali installation failed unexpectedly. I will try with Ubuntu only. For Kali Linux I will still use WSL or a VM. And also if i need a desktop I can still use Kex.

### Ubuntu

I was able to install Ubuntu successfully. The process itself was straight forward but there were some inconveniences. For example, there was no way to tell what was my main windows drive and what was the extra drive for ubuntu. It also would'nt let me use the partition I had set up earlier and used the whole 1TB drive. The installation program would also randomly crash while going through setup. Aside from that ubuntu runs perfectly fine on my computer now.

## Boot Sequence

To boot into Ubuntu I have to go into the BIOS and change the boot order of the drives because I didnt use Windows boot manager. After restarting and entering BIOS I have to go into advanced settings and change, not the boot order, but the specific boot order of UFEI hard drives.