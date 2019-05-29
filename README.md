# arch-sortmirror
You can use "make" and "make install".  
     1	#!/bin/bash  
     2	cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.backup  
     3	sed -i 's/^#Server/Server/' /etc/pacman.d/mirrorlist.backup  
     4	rankmirrors -n 6 /etc/pacman.d/mirrorlist.backup > /etc/pacman.d/mirrorlist  
