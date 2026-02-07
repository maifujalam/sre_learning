Create Virtual machine with Vagrant and VirtualBox
======================================================================
This guide will help you set up a virtual machine using Vagrant and VirtualBox.
Prerequisites
--------------
Before you begin, ensure you have the following installed on your system:
- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
Vagrant Autocomplete Installation
--------------------------------
1. Open your terminal and validate the vagrant and virtual box installation by running:
   ```sh
   vagrant --version
   VBoxManage --version
   virtualbox --version
   ```
2. Run the following command to install Vagrant autocomplete [Optional]:
   ```sh
   vagrant autocomplete install
    ```
3. Default vagrant ssh credential is: vagrant/vagrant [ Only for test env do not use in production ]
4. To enhance your Vagrant experience, you can install autocomplete for your shell. Follow the steps below: [Optional]
    a. For Bash:
        ```sh
        vagrant autocomplete install --shell bash
        ```
    b. For Zsh:
        ```sh
        vagrant autocomplete install --shell zsh
        ```
    c. For Fish:
        ```sh
        vagrant autocomplete install --shell fish
        ```

Setting Up the Virtual Machine
--------------------------------
1. Go to the directory based on your operating system and desired configuration.
   a. For example, to deploy single vm on MAC OS, in environment name "my-server"
       ```sh
       cd VMs/MAC_OS/single_vm/my-server
       ```
    b. For example, to deploy multi vm on MAC OS, in environment name "dev-environment"
       ```sh
       cd VMs/MAC_OS/multi_vm/ceph-cluster/
       ```
2. Check the vagrant vm status
   ```sh
   vagrant status  
   ```
3. Check the vagrant global status
   ```sh
   vagrant global-status
   ```
4. Start the virtual machine:
   ```sh
   vagrant up [ --provision to force provisioning ]
   ```

Managing the Virtual Machine
--------------------------------
- To stop the virtual machine:
  ```sh
  vagrant halt
  ```
- To restart the virtual machine with the updated Vagrant configuration:
  ```sh
   vagrant reload
  ```
-- To hybernate the virtual machine:
  ```sh
  vagrant suspend
  ```
- To resume the virtual machine from hybernation:
  ```sh
  vagrant resume
  ```
- To destroy the virtual machine:
  ```sh
  vagrant destroy [ -f to force. To destroy a single vm, run: vagrant destroy <vm-name> ]
  ```

Connecting to the Virtual Machine
--------------------------------
1. To connect to the virtual machine via vagrant SSH:
  a. Go to the directory where your Vagrantfile is located.
  b. Run the following command:
  ```sh
  vagrant ssh [ <vm-name> for multi-vm setup ]
  ```
2. TO connect with the virtual machine using console:
  a. Go to VirtualBox GUI
  b. Select the VM and click on "Show" to open the console window.
  c. To exit the fromthe control window, use `ctrl`  or `Ctrl + C` or close the window.

3. To ssh into the VM from terminal using VM IP Address.
   a. Open the terminal and run the following command:
   ```sh
   ssh vagrant@<VM_IP_ADDRESS>
   ```
   b. When prompted, enter the password: `vagrant`

Additional Resources
---------------------
For more information on using Vagrant and VirtualBox, refer to the following resources:
- [Vagrant Documentation](https://www.vagrantup.com/docs)
- [VirtualBox Documentation](https://www.virtualbox.org/wiki/Documentation)
Happy Vagranting!
