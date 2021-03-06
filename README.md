This script i'm using on my flash drive with gentoo
---
# Usage
* **-u**  —  Enter users (separated by commas. Example: user1,user2,etc)
* **-d**  —  Directory for user data files (for *.tar.xz. Default: /var/lib/u2tmpfs)
* **-U**  —  Create/Update all *.tar.xz
* **-s**  —  tmpfs size option (Example: 512M, 4G. Default: 512M; Warning: you can use only half of installed RAM!)
* **-o**  —  Use the specified mount options for tmpfs (Default: "mode=755,noatime")
* **-w**  —  Wipe user data on USER_DATA_DIR for current USER (-u user1)

# Example
**1. Only init/update all users data without mounting tmpfs "mount -t tmpfs ...":**
   ~~~bash
   u2tmpfs -u user1,user2 -d /var/lib/u2tmpfs -U
   ~~~
**2. Mount users home dir to tmpfs and extract all users data:**
   ~~~bash
   u2tmpfs -u user1,user2
   ~~~