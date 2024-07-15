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


# setting up the project, here is the answer given by preplexity: 
Okay, let's go through the steps to solve the issue where the IDF_PYTHON_ENV_PATH environment variable is not set.
Activate the ESP-IDF environment:
In the terminal, run the following command to activate the ESP-IDF environment:
text
. $IDF_PATH/export.sh

This will set up the necessary environment variables, including the IDF_PYTHON_ENV_PATH.
Verify the IDF_PYTHON_ENV_PATH:
After activating the ESP-IDF environment, run the following command to check the value of the IDF_PYTHON_ENV_PATH environment variable:
text
echo $IDF_PYTHON_ENV_PATH

This should now show the path to the ESP-IDF Python virtual environment.
Verify the Python version in the virtual environment:
Run the following command to check the Python version in the ESP-IDF virtual environment:
text
python --version

This should match the Python version you have installed on your system.
Try running idf.py again:
Now, try running the idf.py commands (e.g., idf.py build, idf.py menuconfig) again. They should work without any issues related to the Python executable.
If you're still facing issues, you can try the following additional steps:
Ensure the virtual environment is activated:
If the IDF_PYTHON_ENV_PATH variable is set correctly, but you're still facing issues, try activating the virtual environment manually by running the following command:
text
source $IDF_PYTHON_ENV_PATH/bin/activate

This should activate the virtual environment and ensure that the idf.py command can find the correct Python executable.
Check the ESP-IDF installation:
Ensure that your ESP-IDF installation is set up correctly. You can refer to the official ESP-IDF documentation for detailed instructions on setting up the development environment.
Check for any conflicting Python environments:
Make sure there are no other Python environments or virtual environments that might be interfering with the ESP-IDF environment. You can try running which python to see which Python executable is being used by the system.
By following these steps, you should be able to resolve the issue with the IDF_PYTHON_ENV_PATH environment variable not being set. The key is to ensure that the ESP-IDF environment is properly set up and that the Python virtual environment is correctly configured.
