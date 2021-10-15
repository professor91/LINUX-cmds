# LINUX-cmds

# General commands
- mkdir <directory name>		--	Make a new folder
- rm -rf <file/folder name>	--	Delete the file/folder

- ls      -- 	list all files/folders of the directory
- ls -a   --  list of all hiddn folders

- sudo apt-get update
- sudo apt-full upgrade

- cat file_name.extension  -- shows the data of the file
- nano file_name           -- lets you edit the file in terminal



# Pendrive commands

- lsblk                           -- shows lists of all drivers available
- lsblk -fb dev/disk_name         -- show the content of mentioned disk

- sudo mount /dev/disk_name       -- mount the disk
- sudo umount /dev/disk_name      -- unmount the disk

- sudo fdisk -l /dev/disk_name    -- show the filesystem of the disk
- sudo wipefs -a /dev/disk_name   -- erase existing filesystem from the disk

- sudo cfdisk /dev/disk_name      -- change the filesystem of the disk  <br />
                                    |-> choose "dos"                    <br />
                                    |-> choose file system (fat32)      <br /> 
                                    |-> click on "Write"                <br />
                                    |-> "Quit"                          <br />

<h2>converting the filesystem of the disk</h2>
- sudo mkntfs -Q -L "USBNTFS" /dev/partition_name -- to convert in ntfs file system
- sudo mkfs.ext4 -L "USBEXT4" /dev/partition_name -- to convert in ext4 file system

- sudo mkfs.vfat -n "USBFAT32" /dev/partition_name -- to convert in fat32 file system (windows compatible)

- sudo eject /dev/sda

# Create vitual enviroment in python

- python3 -m venv <name of the virtual env folder>	--	create virtual enviroment

- source <name of the virtual env folder)>/bin/activate		--	to activate the enviroment
- deactivate 		--	to deactivate the enviroment

- pip list		--	list all the libraries present in that project
- pip freeze		--	list of all libs of virtaul env for requirements.txt file for new virtual env
- pip freeze > requirements.txt	

  <h2>do not save your projct files in virtual enviroment folder</h2>
- python3 -m venv <name of the virtual env folder> --system-site-packages		--	create a virtual enviroment that contains all the global python libraries


