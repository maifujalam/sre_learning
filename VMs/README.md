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
To enhance your Vagrant experience, you can install autocomplete for your shell. Follow the steps below:
1. Open your terminal.
2. Run the following command to install Vagrant autocomplete:
   ```sh
   vagrant autocomplete install
    ```
3. Default vagrant ssh credential is: vagrant/vagrant [ Only for test env do not use in production ]

Setting Up the Virtual Machine
--------------------------------
1. Go to the directory based on your operating system and desired configuration.
   a. For example, to deploy single vm on MAC OS, in environment name "my-server"
       ```sh
       cd VMs/MAC_OS/single_vm/my-server
       ```
    b. For example, to deploy multi vm on MAC OS, in environment name "ceph-cluster"
       ```sh
       cd VMs/MAC_OS/multi_vm/ceph-cluster/
       ```

2. Initialize the Vagrant environment:
   ```sh
   vagrant init
   ```
3. Start the virtual machine:
   ```sh
   vagrant up
   ```
4. SSH into the virtual machine:
   ```sh
   vagrant ssh
   ```
Managing the Virtual Machine
--------------------------------
- To stop the virtual machine:
  ```sh
  vagrant halt
  ```
- To restart the virtual machine:
  ```sh
   vagrant reload
  ```
- To destroy the virtual machine:
  ```sh
  vagrant destroy [ -f to force. To destroy a single vm, run: vagrant destroy <vm-name> ]
  ```
Additional Resources
---------------------
For more information on using Vagrant and VirtualBox, refer to the following resources:
- [Vagrant Documentation](https://www.vagrantup.com/docs)
- [VirtualBox Documentation](https://www.virtualbox.org/wiki/Documentation)
Happy Vagranting!