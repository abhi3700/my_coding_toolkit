# Virtual Machines

This is about setting up a VM with a preferred OS on existing machine.

The followings could be the needs:

- **Virtualization**: Install OS2 (with arch-1) on OS1 (with arch-1) => Same architecture
- **Emulation**: Install OS2 (with arch-2) on OS1 (with arch-1) => Different architecture

Below is the list of softwares which support this VM:

- GUI-based
  - UTM
  - Parallels
  - VMWare (doesn't support M1 processor)
- CLI-based
  - Lima

> All the softwares support VM based same architecture as host or different architectures (ARM on AMD, AMD on ARM)

## A. Virtualization

Install Ubuntu (ARM) on Mac (ARM)

### A1. `colima`

This is a CLI tool that is built on top of `lima`. It is very easy to use unlike `lima`.

- Install using brew: `$ brew install colima`.
- Commands:
  - `$ colima list` => lists the VMs
  - `$ colima start` => starts the VM
  - `$ colima start --cpu 4 --memory 8` => starts the VM with custom ram & cpu
  - `$ colima stop` => stops the VM
  - `$ colima ssh` => opens the VM's shell like `lima` i.e. get to use linux on top of mac with same ARM hardware.c
  - `$ colima status` => shows the status of VM

    ```sh
    INFO[0000] colima is running using QEMU
    INFO[0000] arch: aarch64
    INFO[0000] runtime: docker
    INFO[0000] mountType: sshfs
    INFO[0000] socket: unix:///Users/abhi3700/.colima/default/docker.sock
    ```

  - `$ colima version` => shows the version of VM

    ```sh
    colima version 0.6.7
    git commit: ba1be00e9aec47f2c1ffdacfb7e428e465f0b58a

    runtime: docker
    arch: aarch64
    client: v24.0.5
    server: v24.0.7
    ```

  - <kbd>ctrl+d</kbd>: Quit the VM's shell
  - `$ colima help` => shows the help

#### Use `docker` inside VM of `colima` like this

```sh
abhi3700@colima:/$ docker version
Client: Docker Engine - Community
 Version:           24.0.7
 API version:       1.43
 Go version:        go1.20.10
 Git commit:        afdd53b
 Built:             Thu Oct 26 09:08:29 2023
 OS/Arch:           linux/arm64
 Context:           default

Server: Docker Engine - Community
 Engine:
  Version:          24.0.7
  API version:      1.43 (minimum version 1.12)
  Go version:       go1.20.10
  Git commit:       311b9ff
  Built:            Thu Oct 26 09:08:29 2023
  OS/Arch:          linux/arm64
  Experimental:     false
 containerd:
  Version:          1.6.25
  GitCommit:        d8f198a4ed8892c764191ef7b3b06d8a2eeb5c7f
 runc:
  Version:          1.1.10
  GitCommit:        v1.1.10-0-g18a0cb0
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```  

And we can also use other docker commands like `docker ps`, `docker images`, etc.

Congrats! 🎉 You have successfully installed `colima` on your Mac M1. And also, you are able to use `docker` inside the VM of `colima`.

### A2. `lima`

> NOTE:
>
> DISCLAIMER: As of 5-Jan-2024, `lima` is not working. It doesn't open SSH connection to the VM instance. Hence, can't use linux inside mac M1 using `lima`.

<details>

<summary>For the sake of knowledge, you may expand this:</summary>

Repo:

Lima launches Linux VMs (CLI-based/controlled) with automatic file sharing and port forwarding (similar to **WSL2**), and containerd.

> Here, the guide is about installing Ubuntu 20.04 OS with ARM processor on Mac M1 (ARM).

- Install `lima` using brew: `$ brew install lima`
- [OPTIONAL] Create `lima.yaml` file & modify as per required Ubuntu version i.e. 20.04 instead of latest (22.04). **Skip this**

```console
❯ mkdir /Users/abhi3700/.lima/default
❯ touch /Users/abhi3700/.lima/default/lima.yaml
❯ code ~/.lima/default/lima.yaml
```

- Select the 'review' option during creating an instance like this:
  <img width="706" alt="image" src="https://user-images.githubusercontent.com/16472948/175220315-7adf13ce-76bf-48a6-a04a-bb413b91982b.png">

Press enter with the option & then the `lima.yaml` of the instance would open using `vim` in terminal. So, in order to edit using `vscode`, exit from here:

```
:qa!
```

Now, your instance is created with `lima.yaml`. So, open this using `vscode`: `❯ code ~/.lima/docker/lima.yaml` & then

- [OPTIONAL] Copy the content from [here](https://gist.github.com/abhi3700/2b41a33575ab425e33199fec1e0b293f) &
- replace the portion below.

![image](https://user-images.githubusercontent.com/16472948/169226669-63bd9ca0-1e02-481c-9ec1-63d613f67e5d.png)

with

```yaml
# 🔵 This file: Ubuntu 20.04 Focal Fossa images
images:
  # Try to use release-yyyyMMdd image if available. Note that release-yyyyMMdd will be removed after several months.
  - location: "https://cloud-images-archive.ubuntu.com/releases/focal/release-20200423/ubuntu-20.04-server-cloudimg-amd64.img"
    arch: "x86_64"
    digest: "sha256:266663b10f788f784a425873086051910084bc08c059bf8e4a9490ce306f8d7e"
  - location: "https://cloud-images-archive.ubuntu.com/releases/focal/release-20200423/ubuntu-20.04-server-cloudimg-arm64.img"
    arch: "aarch64"
    digest: "sha256:8066f5973d9b291ba1e637d7cb98b782abb6f3507f4265482ba6c6270210a736"
  # Fallback to the latest release image.
  # Hint: run `limactl prune` to invalidate the cache
  - location: "https://cloud-images.ubuntu.com/releases/20.04/release/ubuntu-20.04-server-cloudimg-amd64.img"
    arch: "x86_64"
  - location: "https://cloud-images.ubuntu.com/releases/20.04/release/ubuntu-20.04-server-cloudimg-arm64.img"
    arch: "aarch64"
```

- Install OS using `$ limactl start`

  > It installs the set "Ubuntu 20.04" as `lima.yaml` file in `default` instance.

- After this, the directory looks like this, where only `default` instance/VM is created.
  <img width="140" alt="image" src="https://user-images.githubusercontent.com/16472948/169227264-a141213e-3f94-4302-a8e6-ebad49b6b4a8.png">

- View the installed VM using `$ limactl list`
  <img width="748" alt="image" src="https://user-images.githubusercontent.com/16472948/169227511-eca1acb3-66e5-415a-a9cf-512ba23f4219.png">

- Now, to start the VM use `$ limactl start`
  > If no instance name is provided, then it starts the `default` instance.

<img width="1277" alt="image" src="https://user-images.githubusercontent.com/16472948/169227771-f545b404-b79a-4f25-88ab-1b25dd28e484.png">

- Open the VM's shell using `$ lima`
  > If no instance name is provided, then it opens the `default` instance.

<img width="304" alt="image" src="https://user-images.githubusercontent.com/16472948/169227961-40558575-4d9f-4752-9675-d2c9bfa79432.png">

- For a non-default VM shell, use `$ limactl shell <instance-name>` like `$ limactl shell docker`.
  <img width="288" alt="image" src="https://user-images.githubusercontent.com/16472948/175223465-ff39d0e4-08e1-4685-819e-c732eeb28289.png">

- Close the VM using <kbd>ctrl+d</kbd> i.e. logout.
  <img width="363" alt="image" src="https://user-images.githubusercontent.com/16472948/169228058-cd61562d-d6fc-408e-9502-37254c4e0eea.png">

- Shutdown the VM using `$ limactl stop`
  > If no instance name is provided, then it shutdown the `default` instance.

> NOTES: <br/>
>
> - It is recommended to use the VM's drive (i.e. 100 GB by default) rather than using the files (to write to). Because it would be slow to process (read/write). <br/>
> - Otherwise, in order to write to the Mac files from inside VM, set this param as `true` like this:
>   <img width="502" alt="image" src="https://user-images.githubusercontent.com/16472948/169231978-50376883-6342-464a-bf0c-38534ee76ca0.png">

> - The home directory of VM is `~`, NOT the `/Users/abhi3700` unlike the case of Mac where both are same. In the fig. below, the content of `~` is different than `/Users/abhi3700` inside VM.
>   <img width="1107" alt="image" src="https://user-images.githubusercontent.com/16472948/169232449-aceffaa0-72fa-4edc-830a-81d89ad37bab.png">

<img width="982" alt="image" src="https://user-images.githubusercontent.com/16472948/169232858-d9697b4b-604b-4357-ab50-d1c8b283d12b.png">

Read [more](https://github.com/lima-vm/lima).

#### Use VSCode editor

1. Please ensure your VSCode is installed properly on your Mac, like [this](https://github.com/abhi3700/my_coding_toolkit/blob/master/vsc_all.md).

2. Install the docker CLI using `brew`: `$ brew install docker`

3. Create Linux VM with Dockerd (following instructions from [Kevin O’Brien – Utilizing Docker CLI without Docker Desktop](https://itnext.io/utilizing-docker-cli-without-docker-desktop-4933f3473d5e))
   - Download `docker.yaml` file: `$ curl https://raw.githubusercontent.com/lima-vm/lima/master/examples/docker.yaml -O`
   - Create a docker based instance with this: `❯ limactl start ./docker.yaml` & then follow the installation above for custom Ubuntu OS version (20.04, 22.04, ...).
   - After modifying `lima.yaml` inside the `docker` named instance, please continue the installation like this: `$ limactl start docker`
     <img width="1274" alt="image" src="https://user-images.githubusercontent.com/16472948/175221985-623ccfea-7071-4642-8e23-c0cab307a716.png">
   - Enable SSH on the VM instance created: `$ sudo systemctl enable ssh.service`

So, the Lima VM is stopped or logged-out, the SSH service remains enabled unless stopped/disabled inside VM's shell [More about SSH on Ubuntu](https://www.cyberciti.biz/faq/howto-start-stop-ssh-server/). The status can be checked using this:

```console
sudo systemctl status ssh
```

4. Ensure the `writeable` flag to the `lima.yaml` of the instance (being used i.e. `docker`). And then, restart using `❯ limactl stop docker` >> `❯ limactl start docker`
5. On a separate terminal tab, create context for Docker-CLI to connect to dockerd running in the VM:

Create (one-time):

```
❯ docker context create lima --docker "host=unix://${HOME}/.lima/docker/sock/docker.sock"
```

Use `lima` context in docker (whenever switched to other docker context):

```
❯ docker context use lima
```

View the current docker context (being used):
<img width="1107" alt="image" src="https://user-images.githubusercontent.com/16472948/175228165-4c4be786-bb50-4ef0-90f9-620f6dd702e8.png">

6. Open VScode: - Add SSH server like this:
   <img width="539" alt="image" src="https://user-images.githubusercontent.com/16472948/175229319-3c39fa9e-485f-4e74-a328-ec74f2b91281.png">

To view the exact url of the VM instance, view from this:
<img width="776" alt="image" src="https://user-images.githubusercontent.com/16472948/175229992-be64faa7-7824-4728-b6b2-1dd139c710d0.png">

</details>

## B. Emulation

### [UTM](https://mac.getutm.app/) | Install Ubuntu (AMD) on Mac (ARM)

Here, the guide is about installing Ubuntu 20.04 (using desktop ISO) with intel/AMD processor on Mac M1.

There are softwares which do not support M1 processor for which this emulation is to be done.

#### Step-1: Home page in UTM App

<img width="808" alt="image" src="https://user-images.githubusercontent.com/16472948/168827366-963d76e9-0c4a-4a22-bc07-a562323c4e29.png">

#### Step-2: Create a New VM

<img width="808" alt="image" src="https://user-images.githubusercontent.com/16472948/168827661-cf13a539-de42-416a-bcf3-fa5d8e438f84.png">

#### Step-3: Select Emulate option

<img width="580" alt="image" src="https://user-images.githubusercontent.com/16472948/168828071-8238078a-e744-4baf-8edb-948c9fd7783c.png">

#### Step-4: Select OS

<img width="530" alt="image" src="https://user-images.githubusercontent.com/16472948/168828370-d6afe2b6-1a06-4313-a058-8f47ff0577cc.png">

#### Step-5: Browse ISO file for Ubuntu 20.04

<img width="510" alt="image" src="https://user-images.githubusercontent.com/16472948/168828652-cf67a815-1e68-4260-ac19-78d6cdd6025e.png">

#### Step-6: Select the downloaded ISO file

<img width="690" alt="image" src="https://user-images.githubusercontent.com/16472948/168828963-d383d5a1-abee-4d50-a373-044b5b2de970.png">

#### Step-7: Configure Hardware

Here, we can force the CPU cores as per the need later so that the VM runs a little faster.

> NOTE: Normally, the emulation is slower than virtualization

<img width="485" alt="image" src="https://user-images.githubusercontent.com/16472948/168829131-99a57289-b429-4ed9-8364-0a3bb9f2ee09.png">

#### Step-8: Configure Storage

<img width="492" alt="image" src="https://user-images.githubusercontent.com/16472948/168829390-b859c6d3-5772-4bf0-ac1c-216bac8ec82f.png">

#### Step-9: Configure Shared Directory

Not necessary before installation

<img width="510" alt="image" src="https://user-images.githubusercontent.com/16472948/168829584-449aa7d3-770f-450b-b3e2-32ade6965465.png">

#### Step-10: Give Custom name

This is the name by which it would be saved within `./utm` directory on Mac.

<img width="494" alt="image" src="https://user-images.githubusercontent.com/16472948/168829979-8665d3d1-48d6-4961-adc6-0f28904c66d2.png">

And then <kbd>Save</kbd> it.

#### Step-11: View Saved

This is how it looks like:

<img width="1278" alt="image" src="https://user-images.githubusercontent.com/16472948/168830472-61cbfd06-2fda-41ba-a92c-1dee3d92a644.png">

#### Step-12: Start

Go for the 1st option

<img width="821" alt="image" src="https://user-images.githubusercontent.com/16472948/168830929-e10ae98e-8c34-4684-bc88-cbe80c4c6bf3.png">

And follow the instruction for installation.

View the Screens post installation

#### References | Screen: Information

<img width="828" alt="image" src="https://user-images.githubusercontent.com/16472948/168831755-fcc517f2-3a7d-4cfa-a326-6609391791cb.png">

#### References | Screen: System

<img width="828" alt="image" src="https://user-images.githubusercontent.com/16472948/168831979-5b837eb3-1112-4b8f-9011-ba19550689e3.png">

#### References | Screen: QEMU

<img width="830" alt="image" src="https://user-images.githubusercontent.com/16472948/168832050-e2dab5a6-5674-41f4-946f-c756ad3ca8ee.png">

#### References | Screen: Display

<img width="831" alt="image" src="https://user-images.githubusercontent.com/16472948/168832148-fde71769-bded-4271-9ef3-45497d573921.png">

#### References | Screen: Input

<img width="834" alt="image" src="https://user-images.githubusercontent.com/16472948/168832699-80ef5519-920a-4e30-acb5-2ad6e96e36e3.png">

#### References | Screen: Network

<img width="823" alt="image" src="https://user-images.githubusercontent.com/16472948/168832994-dff3317d-5ba7-431a-b059-f3f621f0c1bc.png">

#### References | Screen: IP Config

<img width="822" alt="image" src="https://user-images.githubusercontent.com/16472948/168833260-6ae75c00-7ed6-41ab-ab82-072ef0389d8e.png">

#### References | Screen: Sound

<img width="824" alt="image" src="https://user-images.githubusercontent.com/16472948/168833300-a7e67269-9dd3-420f-8ece-7ee57cbb8cd3.png">

#### References | Screen: Sharing

<img width="825" alt="image" src="https://user-images.githubusercontent.com/16472948/168833630-5f5eebff-a622-4364-befa-62f09cb0df71.png">

#### References | Screen: IDE Drive Disc

Before installation, this Disc option remains below the removable drive (CD/DVD) i.e. ISO, from where the ubuntu file is loaded for installation.

After installation, the CD/DVD can be cleared from below or "removable drive" option can be put down to this Disc option, so that after OS reboot it loads the installed OS.

<img width="837" alt="image" src="https://user-images.githubusercontent.com/16472948/168833757-8cd70990-6b96-44b2-af12-63ef6e7a2fe8.png">

#### References | Screen: IDE Drive Removable

<img width="824" alt="image" src="https://user-images.githubusercontent.com/16472948/168834756-5f014bf2-8201-43e9-8ce6-8918c333662f.png">

#### References | Screen: EFI Variables

<img width="825" alt="image" src="https://user-images.githubusercontent.com/16472948/168834824-475761c3-d0c5-4088-967c-be3737c154dc.png">

#### Step-13: Shared Directory

After installation, to allow the shared directory to be shown in the installed OS i.e. Ubuntu, follow these sub-steps on Ubuntu:

1. `$ sudo apt install spice-vdagent spice-webdavd davfs2`
2. Restart the VM
