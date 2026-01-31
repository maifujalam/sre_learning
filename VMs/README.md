Create Virtual machine with Vagrant and VirtualBox
======================================================================
This guide will help you set up a virtual machine using Vagrant and VirtualBox.
Prerequisites
--------------
Before you begin, ensure you have the following installed on your system:
- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
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
  vagrant destroy
  ```
Additional Resources
---------------------
For more information on using Vagrant and VirtualBox, refer to the following resources:
- [Vagrant Documentation](https://www.vagrantup.com/docs)
- [VirtualBox Documentation](https://www.virtualbox.org/wiki/Documentation)
Happy Vagranting!