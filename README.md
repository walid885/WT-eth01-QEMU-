# WT-eth01-QEMU-
Emulation of the wt-eth01 using the QEMU on Ubuntu 

# setting up and downloading the QEMU using ubuntu 
refer to this link of the documentation : https://wiki.qemu.org/Hosts/Linux#Building_QEMU_for_Linux

# after setting up the esp_idf extension, tried to create the new project, but there is an issue , it requiered the installation of the esp-idf itself. 

here is the installation process down below: taking track of the data of the link of documentation:  
https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/linux-macos-setup.html

# problem in Step two, caused by the --recursive flag, 
I did some research, and trying this solution found in stack overflow : link: https://stackoverflow.com/questions/21277806/fatal-early-eof-fatal-index-pack-failed 

note: problem solved with setting an unlimited packedGitLimit, I guess the EOF was caused by the defalut memory limit in git configuration. 

# problem in Step two, caused by the --recursive flag, 
in order to comeplet the Setup, you must completee the installation of the esp_idf , from the esp documentation, and then completing the installation via the esp extension, so that the get to recgonize each other 
=> this is configuration of the setup step is done ! 