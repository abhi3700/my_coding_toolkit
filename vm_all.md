# Virtual Machines

This is about setting up a VM with a preferred OS on existing machine.

The followings could be the needs:

A. Virtualization: Install OS2 (with arch-1) on OS1 (with arch-1) => Same architecture
B. Emulation: Install OS2 (with arch-2) on OS1 (with arch-1) => Different architecture

## B. Install Ubuntu (AMD) on Mac (ARM)

Here, the guide is about installing Ubuntu 20.04 (using desktop ISO) with intel/AMD processor on Mac M1.

There are softwares which do not support M1 processor for which this emulation is to be done.

### Step-1: Home page in UTM App

<img width="808" alt="image" src="https://user-images.githubusercontent.com/16472948/168827366-963d76e9-0c4a-4a22-bc07-a562323c4e29.png">

### Step-2: Create a New VM

<img width="808" alt="image" src="https://user-images.githubusercontent.com/16472948/168827661-cf13a539-de42-416a-bcf3-fa5d8e438f84.png">

### Step-3: Select Emulate option

<img width="580" alt="image" src="https://user-images.githubusercontent.com/16472948/168828071-8238078a-e744-4baf-8edb-948c9fd7783c.png">

### Step-4: Select OS

<img width="530" alt="image" src="https://user-images.githubusercontent.com/16472948/168828370-d6afe2b6-1a06-4313-a058-8f47ff0577cc.png">

### Step-5: Browse ISO file for Ubuntu 20.04

<img width="510" alt="image" src="https://user-images.githubusercontent.com/16472948/168828652-cf67a815-1e68-4260-ac19-78d6cdd6025e.png">

### Step-6: Select the downloaded ISO file

<img width="690" alt="image" src="https://user-images.githubusercontent.com/16472948/168828963-d383d5a1-abee-4d50-a373-044b5b2de970.png">

### Step-7: Configure Hardware

Here, we can force the CPU cores as per the need later so that the VM runs a little faster.

> NOTE: Normally, the emulation is slower than virtualization

<img width="485" alt="image" src="https://user-images.githubusercontent.com/16472948/168829131-99a57289-b429-4ed9-8364-0a3bb9f2ee09.png">

### Step-8: Configure Storage

<img width="492" alt="image" src="https://user-images.githubusercontent.com/16472948/168829390-b859c6d3-5772-4bf0-ac1c-216bac8ec82f.png">

### Step-9: Configure Shared Directory

Not necessary before installation

<img width="510" alt="image" src="https://user-images.githubusercontent.com/16472948/168829584-449aa7d3-770f-450b-b3e2-32ade6965465.png">

### Step-10: Give Custom name

This is the name by which it would be saved within `./utm` directory on Mac.

<img width="494" alt="image" src="https://user-images.githubusercontent.com/16472948/168829979-8665d3d1-48d6-4961-adc6-0f28904c66d2.png">

And then <kbd>Save</kbd> it.

### Step-11: View Saved

This is how it looks like:
  
<img width="1278" alt="image" src="https://user-images.githubusercontent.com/16472948/168830472-61cbfd06-2fda-41ba-a92c-1dee3d92a644.png">

### Step-12: Start

Go for the 1st option

<img width="821" alt="image" src="https://user-images.githubusercontent.com/16472948/168830929-e10ae98e-8c34-4684-bc88-cbe80c4c6bf3.png">

And follow the instruction for installation.

View the Screens post installation

### References | Screen: Information

<img width="828" alt="image" src="https://user-images.githubusercontent.com/16472948/168831755-fcc517f2-3a7d-4cfa-a326-6609391791cb.png">

### References | Screen: System

<img width="828" alt="image" src="https://user-images.githubusercontent.com/16472948/168831979-5b837eb3-1112-4b8f-9011-ba19550689e3.png">

### References | Screen: QEMU

<img width="830" alt="image" src="https://user-images.githubusercontent.com/16472948/168832050-e2dab5a6-5674-41f4-946f-c756ad3ca8ee.png">

### References | Screen: Display

<img width="831" alt="image" src="https://user-images.githubusercontent.com/16472948/168832148-fde71769-bded-4271-9ef3-45497d573921.png">

### References | Screen: Input

<img width="834" alt="image" src="https://user-images.githubusercontent.com/16472948/168832699-80ef5519-920a-4e30-acb5-2ad6e96e36e3.png">

### References | Screen: Network

<img width="823" alt="image" src="https://user-images.githubusercontent.com/16472948/168832994-dff3317d-5ba7-431a-b059-f3f621f0c1bc.png">

### References | Screen: IP Config...

<img width="822" alt="image" src="https://user-images.githubusercontent.com/16472948/168833260-6ae75c00-7ed6-41ab-ab82-072ef0389d8e.png">

### References | Screen: Sound

<img width="824" alt="image" src="https://user-images.githubusercontent.com/16472948/168833300-a7e67269-9dd3-420f-8ece-7ee57cbb8cd3.png">

### References | Screen: Sharing

<img width="825" alt="image" src="https://user-images.githubusercontent.com/16472948/168833630-5f5eebff-a622-4364-befa-62f09cb0df71.png">

### References | Screen: IDE Drive Disc

Before installation, this Disc option remains below the removable drive (CD/DVD) i.e. ISO, from where the ubuntu file is loaded for installation.

After installation, the CD/DVD can be cleared from below or "removable drive" option can be put down to this Disc option, so that after OS reboot it loads the installed OS. 

<img width="837" alt="image" src="https://user-images.githubusercontent.com/16472948/168833757-8cd70990-6b96-44b2-af12-63ef6e7a2fe8.png">

### References | Screen: IDE Drive Removable

<img width="824" alt="image" src="https://user-images.githubusercontent.com/16472948/168834756-5f014bf2-8201-43e9-8ce6-8918c333662f.png">

### References | Screen: EFI Variables

<img width="825" alt="image" src="https://user-images.githubusercontent.com/16472948/168834824-475761c3-d0c5-4088-967c-be3737c154dc.png">

### Step-13: Shared Directory

After installation, to allow the shared directory to be shown in the installed OS i.e. Ubuntu, follow these sub-steps on Ubuntu:

1. `$ sudo apt install spice-vdagent spice-webdavd davfs2`
2. Restart the VM
 
