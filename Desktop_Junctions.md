# Desktop Storage

![View of My Computer](http://i.jhd5.net/2017/04/2017-04-26_20-13-32.png)

The storage situation on my desktop is stupid. The main C: drive is too small, but my compter can't boot off NVMe. Since buying another SATA SSD is a waste of money, I've restored to a few tricks in order to make this work.

It's still fucking ugly though.

## The main Players

Here's the list of drives who are participating in this travesty.

* C: - System/Boot Drive (256GB SSD)
* D: - Previous Boot Drive (256GB SSD)
* E: - junk (1TB HDD)
* F: - Scratch Disk, anything temporary that doesn't need backups or fast storage (2TB Storage Space, no mirror)
* G: - Games. (2TB Storage Space)
* H: - The drive I had purchased hoping to replace C:, but that didn't pan out. Still fast af. (1TB NVMe)
* Q: - Anything that doesn't need speed and can be offloaded from C: (1TB WSS)

The Windows Storage Space cluster is made up off 2x2TB and 2x3TB Western Digital Black HDDs.

## System Configuration

The page file is on D:.

## Application Configuration

All game clients are configured to install games to G:. The Epic Games Launcher required a few additional junctions.

Amazon Drive is mounted on Q:.

## NTFS Junction to Hell

In order to regain space on my C: drive, I've moved a the larger space offenders onto other drives. This is a running list of the junctions.

* C:\src -> H:\src
* C:\Windows\Installer -> Q:\Windows\Installer
* C:\Users\John\.nuget -> D:\__JOHN\.nuget
* C:\Users\John\AppData\Local -> D:\__JOHN\AppData\Local
* C:\Users\John\AppData\Remote -> D:\__JOHN\AppData\Remote
* C:\Program Files\Epic Games\Launcher\PatchStaging -> G:\Unreal\PatchStaging
* C:\Program Files\Epic Games\Launcher\VaultCache -> G:\Unreal\VaultCache