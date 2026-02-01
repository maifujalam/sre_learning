Configure a Single macOS VM
=========================== 
This guide will help you set up a single macOS virtual machine (VM) using popular virtualization software. Follow the steps below to get your macOS VM up and running.
Prerequisites
-------------
- MAC OS with 16GB RAM minimum 
- Virtualization Software (e.g., VirtualBox)
- Vagrant installed

Configure the VM
-----------------
1. Edit the Vagrant file to update the Hardware settings as per your requirements.  
   Example:-  
    a. To change the cpu core count to 4.Make:-  **CPU_COUNT = 4**
    b. To change the memory size to 4GB.Make:-  **MEMORY_SIZE = "4096"**
    c. To change to number of additional disks to 2. Make:-  **ADDITIONAL_DISK_COUNT = 2**  
    d. To change the each additional disk size to 3GB. Make:-  **ADDITIONAL_DISK_SIZE = "3GB"**  
    e. To change the private vm network IP address to. Make:-  **NETWORK_IP = 192.168.1.5**"
    f. The VM is created with default disk of 64GB.There is no option to change the default disk size as of now.
        This is virtual size and will be growing up to 64GB on demand.
    g. Additional OS cab be chosen from below for APPLE M-series CPU and Virtual Box provider.
       https://portal.cloud.hashicorp.com/vagrant/discover?architectures=arm64&providers=virtualbox

2. Open a terminal and navigate to the directory containing your Vagrantfile.
3. Run the following command to start the VM:  
  ```bash
   vagrant up
  ```
4. Once the VM is up and running, you can access it using:  
   ```bash
   vagrant ssh
   ```
5. To stop the VM, use:
   ```bash
    vagrant halt
   ```
