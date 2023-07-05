---
template: note
---
![tp.web.random_picture](https://images.unsplash.com/photo-1494500764479-0c8f2919a3d8?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjYyOTIwNzkz&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-09-11) | (time:: 23:56) | (weather:: Vadodara: 🌦   +30°C ↑11km/h)

# Linux Directory Structure
![[Screenshot 2022-09-12 at 00.58.27.png]]
## `/`
Root Directory.

### `/bin`
Contains binaries or executables that are essential to the entire operating system. You can run these binaries from the command line anytime. Commands like `gzip`, `curl`, or `ls` are some examples that belong to this directory.

### `/sbin`
Contains system binaries that should only be executed by the `root` user. Commands like `mount` or `deluser`.

### `/lib`
Many of these binaries may share common libraries which are stored inside this directory. 

### `/usr`
This directory contains **non-essential** binaries inside its sub-directories `/bin` and `/sbin`.
#### `/bin`
#### `/sbin`
#### `/local`
This directory contains any binary that you've compiled manually.

### `/etc`
To customize the behavior of software on your system. The `etc` stands for *Et cetra* or *Editable Text Config*.

### `/boot`
Contains files needed to boot the system like the Linux kernel itself.

### `/dev`
It stands for **device** files. Here, you can interface with hardware or drivers as if they are regular files.

### `/var`
Contains variable files that will change as the operating system is used, like logs and cache files.

### `/tmp`
Contains temporary files that won't be persisted between reboots.

### `/proc`
This directory is an **illusionary** file system that doesn't actually exist on the disk. It is created in memory on the fly by the Linux kernel to keep track of running processes.

## Find binary location
```bash
which curl # outputs /usr/bin/curl
```

## References
- [macOS File System](https://developer.apple.com/library/archive/documentation/FileManagement/Conceptual/FileSystemProgrammingGuide/FileSystemOverview/FileSystemOverview.html)

---
## Internal Links
[[2022-09-11]], [[Operating Systems]], [[Linux]]