# tutorials

How to connect ssh from linux virtual machine to host pc with VirtualBox

1. Open VirtualBox and click once on the virtual machine you want to change
2. Press on settings button (Make sure you do not have a saved state for this virtual machine)
   ![image](https://github.com/user-attachments/assets/a75f4cec-5b85-4609-b2d0-3fed391b7641)
3. Go to the network settings (Make sure expert mode in enabled!)
   ![image](https://github.com/user-attachments/assets/4547fa42-c0fc-45b6-aac4-d984959034d5)
4. If you don't have an adapter of the NAT type go to the first empty adapter and enable it and choose NAT type (Don't do anything if you do have a NAT adapter)
5. Go to Port Forwarding rules on this adapter's settings and create a rule that has the exact same info as here <img width="636" height="202" alt="image" src="https://github.com/user-attachments/assets/8e623596-70a2-41bd-81f2-1ef2ec78ab7c" />
6. Click ok, close the settings and run the Linux VM
7. In the terminal of the VM run the command sudo apt-get update; sudo apt-get install openssh-server   (For Ubuntu or debian distros) or the equivalent if you have another package installer
8. if you have linux on host machine just do ssh -p 3022 <vm_username>@127.0.0.1
   if you have windows on host machine first check if you have ssh installed by running ssh in command prompt or powershell. If you do not, find how to install it (hint: optional features). after that you can run the same command ssh -p 3022 <vm_username>@127.0.0.1
