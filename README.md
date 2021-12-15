# LINUX-cmds

- sudo apt-get update         -- download new updates
- sudo apt-full upgrade       -- install new updates

# Good First Commands

- pwd                         --  will Print working directory (the directory in which you are currently in)
- cd directoryName            --  will open the directoryName directory (directory is also called folder)

- ls                          -- 	list all files/folders of the directory
- ls -a                       --  list of all hidden files & folders (hidden file starts with .)
- ls -l                       --  list of all files with all details

- mkdir directory_name		      --	Make a new directory/folder
- rm filename                  --	Delete the file
- rm -f filename               --  Force deletes the file
- rm -rf directoryname         --  Deletes a directory and all it's files

# Utility commands

- history                     --  shows list of all commands that you have executed on the terminal
- clear                       --  clears the terminal screen
- Ctrl + L                    --  scrolls the terminal clean
                                  sometimes you don't want to use clear command and clear the previously used commands from screen but 
                                  just scroll everything up so it looks clean as new

- find /directoryName -name name_of_file                      --  to find a file
- find /directoryName -type type_of_file -name name_of_file   --  to find a specific type of file

- man command_name            --  display's user manual for the command
- whatis command_name         --  tells about the command

- alias alias_name='command'  -- assign a new alias to an existing command
- unalias alias_name          -- unassign the assigned alias
      Eg. alias list='ls'
          now if you type list, it will work as ls, to undo it use 
          unalias list

# File commands

- touch filename               --  creates a file titled filename
                                  if you use touch command and specify name of an existing file/directory
                                  then it will change the timestamp of the file

- file file_name               --  shows the description of the file

- cat file_name.extension     -- shows the content of the file mentioned
- nano file_name              -- lets you edit the file in terminal


# Disk commands (Pendrive)

- lsblk                           -- shows lists of all drivers available
- lsblk -fb dev/disk_name         -- show the content of mentioned disk

- sudo mount /dev/disk_name       -- mount the disk
- sudo umount /dev/disk_name      -- unmount the disk

- sudo fdisk -l /dev/disk_name    -- show the filesystem of the disk
- sudo wipefs -a /dev/disk_name   -- erase existing filesystem from the disk

- sudo cfdisk /dev/disk_name      --  change the filesystem of the disk  <br />
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


