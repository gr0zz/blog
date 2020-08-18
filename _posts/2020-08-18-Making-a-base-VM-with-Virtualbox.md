Making a base VM with Virtualbox

## Differences in copying the VM folder, snapshots, cloning machine in VirtualBox
### Copying the VM Folder. 

Copying the folder is more of a back up option. This is a true back up of the machine. The UUIDs and everything else will be the same. You won't be able run the machine if you try to add it in VirtualBox. You will have to remove and possibly delete the original machine if you do this option. It's not really a big deal if you just save it as a back up to restore from later.

### Snapshotting the Machine

Think of snapshots as a point in time. They are used if you want to make a small change and then merge or revert after you tested the change. Snapshots aren't really useful for a "Base VM" if you need the UUIDs and MAC addresses to change. 

### Cloning the VM

Cloning the VM is as close to copying the folder as you can get. When you clone the machine, the UUIDs and MAC addresses change. If the machine OS relies on Windows activation or GRUB for booting, you might have problems if you don't keep the MAC address. Don't worry, you are able to keep them in cloning. 

To me cloning is the best way to go. I usually use a Linux guest OS so I don't really have the same worries you would have with a Windows machine. 
One thing before we begin

Before you do any of the steps below:

- Install the OS and all the programs you like

- set up the configs 

This will be the one and only time you have to do them. Save for install VirtualBox Guest additions. You'll have to do that with each new machine. 

### How to copy a machine folder

This is pretty simple. 

1. Find the folder where your VMs are installed to.

2. On Windows it's usually: ``C:\Users\{User}\VirtualBox VMs``

3. On Linux it's usually: ``/home/{user}/VirtualBox VMs``

4. On MacOS it's probably in your home directory in the "VirtualBox VMs" folder.

5. Copy and paste the folder into wherever you want to store it until it's needed again. It's that easy. 

### How to snapshot a machine. 

1. Open VirtualBox; you'll see a list of all your virtual machines. Then select the one you would like to snapshot or make your base machine. 
 
![8a4885f3b58b34276a0b295a29417376.png]({{'/assets/1ea17b73d2084457835c900798b7b50b.png'}})

2. Click the hamburger menu and select "Snapshots". You'll get this screen:

![d12176af5336d44f54e953ff7e0a60aa.png]({{'/assets/65750a9ffe24482b9694e0e0c0ff2901.png'}}))

3. Click the "Take" button to create a snapshot. Name it. Then you'll have your snapshot. You can delete and restore after the snapshot is taken. 

### How to clone a machine
1. Again open VirtualBox, select the machine you want to clone, click the hamburger menu, and select "Snapshots". You should be back at this screen:

    ![8f137274fb2e5fb26fd326e8065f9c70.png]({{'/assets/14ec3eadc6c9410eab485c92157b7188.png'}})

2. Click the "Clone" button you'll get this screen:

![a056a72fc20b5344a96a755e252c508f.png]({{'/assets/4eee543962904caebce4aa5e185b646d.png'}})

Name your machine; check the "Keep Disk Names" and "Keep Hardware UUIDs" if needed.
In the MAC Address Policy drop down choose "Generate New MAC addresses for all adapters"

Just follow the wizard to completion and you'll have your clone. It'll appear in your machine list after it's finished cloning. 