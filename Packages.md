# Packages
A Package is a collection of lots of files compiled together.

A linux distribution already comes with pre-approved sources to get packages from and this is how it installs all base packages you see on your system. on Debian system, this source file is in /etc/apt/sources.list file.

Compressing a file in linux:-
    - gzip mycoolfile       -   compresses the file with end extension .gz
    - gunzip mycoolfile.gz  -   decompresses the file
    
gzip cannot add multiple files into one archive. For this we have tar
    - tar cvf mytarfile.tar mycoolfile1 mycoolfile2
        c   - create
        v   - tell the program to be verbose and let us know what it is doing
        f   - the filename of the tar file comes after this option
    - tar xvf mytarfile.tar
        x   - extract
        v   - tell the program to be verbose and let us know what it is doing
        f - the file you want to extract

if you have a file in format myfile.tar.gz you have to decompress it outside to in
or you can use tar only with z
    - tar czf myfile.tar.gz
    - tar xzf file.tar


rpm and dpkg
    .rpm - Red Hat based
    .deb - Debian based

    - Installing a package
        -   dpkg -i some_deb_package.deb
        -   rpm -i some_rpm_package.rpm

    - Remove a package
        -   dpkg -r some_deb_package.deb
        -   rpm -e some_rpm_package.rpm

    - List installed packages
        -   dpkg -l
        -   rpm -qa

yum and apt
    yum - for Red Hat
    apt - for Debian
    
    - Installing a package
        -   apt install package_name
        -   yum install package_name
    
    - Remove a package
        -   apt remove package_name
        -   yum erase package_name
    
    - Updating packages for a repository
        -   apt update; apt upgrade
        -   yum update

    - Get info about installed packages
        -   apt show package_name
        -   yum info package_name


Compiling Source Code
    - build_essential:  software to install the tools that will allow you to compile source code
    - then extract the contents of package file from, most likely, .tar.gz file
    - Depending on what compilation method is used, we'll have to use different commands, such as cmake etc
    
    - ./configure - inside package content files, this will check if all the required dependencies are on our system
    - make - inside package content there is Makefile that contains rules to building the software.
    
    - now you can use "sudo make install" / "sudo make uninstall" but this way you won't know what all changes are
      made on your system and latter command may not be able to uninstall it all
    - so use "sudo checkinstall", this command will make a .deb file that we can easily install and uninstall
