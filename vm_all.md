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

And then <kbd>Save</kbd it.

