# scripts-go
Create a golang program that prints hello

### Pre-requirements

* [Vagrant](https://www.vagrantup.com/downloads)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

### How to use this repo

- Clone
- Build
- Manual check

---

### Clone the repository

```
git clone https://github.com/viv-garot/scripts-go.git
```

### Change directory

```
cd scripts-go
```

### Build the Box

```
vagrant up
```

### Sample output

```
vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Importing base box 'vivien/bionic64'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'vivien/bionic64' version '21.07.06' is up to date...
==> default: Setting the name of the VM: scripts-go_default_1626183188856_46312
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    
[...]

    default: 2021-07-13 13:34:17 (9.56 MB/s) - ‘terraform_0.12.25_linux_amd64.zip’ saved [16736906/16736906]
    default: Archive:  terraform_0.12.25_linux_amd64.zip
    default:   inflating: terraform
    default: /home/vagrant
==> default: Running provisioner: file...
    default: ./hello.go => hello.go
==> default: Running provisioner: shell...
    default: Running: /var/folders/cl/pb51l2dx2050qg0vpbwg_tv40000gq/T/vagrant-shell20210713-88127-z9d09y.sh
```

### Check the program has been compiled successfully

```
vagrant ssh -c "./hello"
```

### Sample output

```
vagrant ssh -c "./hello"
hello world
Connection to 127.0.0.1 closed.
```
