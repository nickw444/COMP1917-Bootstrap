# Welcome To COMP1917
Get programming in less than 10 minutes

## What is this
This repository is designed to help new programmers get up and programming in a matter of minutes. Over the years, I've seen some interesting things COMP1917 students do to program on their own computers, which only makes the development process really hard. These include:

 - Editing code on your local machine, uploading code to CSE servers, compiling and running on CSE servers.
 - Editing code on CSE servers using Nano, compiling on CSE servers, running on CSE servers. 
 - Editing code on a Windows or OSX machine in a GUI Text Editor, drag and dropping files into a Ubuntu virtual machine, compiling within

There are many more weird things I've seen people do, none of which are required.

## Introducing Vagrant
Vagrant is a tool which takes care of provisioning virtual machines. Vagrant is able to create a virtual machine, share folders between the host, and provide easy ways to connect to it. 

This repository has the following goals:

- Setup a headless virtual machine (Ubuntu 15)
- Shares the folder "./work" into the directories ~/ and /work
- Installs commonly used tools, including gcc, gdb and valgrind.

## Getting Started
You only need to follow these steps once for every computer you work on. 

### 1. Install Virtualbox on your computer.
[Download and install Virtualbox](https://www.virtualbox.org/wiki/Downloads) on your computer. 
Vagrant uses Virtualbox as the backend hypervisor. 

### 2. Install Vagrant on your computer
Head on over to the [Vagrant downloads page](https://www.vagrantup.com/downloads.html) and 
pick up the latest copy of Vagrant. 

### 3. There is no step 3. You're done. Continue onto the "Using Vagrant" section

## Using Vagrant
### 1. Power on the Machine
Open a terminal. Type:

```
cd <path/to/the/directory/of/this/repository>
```

You must replace the `<path/to/the/directory...` with the path where you downloaded 
this repository to. 

Type:

```
vagrant up
```

If this is the first time `vagrant up` is being run, it may take a bit longer, because it's performing
some machine provisioning.

Note: You only need to perform `vagrant up` if you have restarted your computer, or explicitly ran 
`vagrant destroy` or `vagrant halt`. 

### 2. Connect to the machine
In the same terminal, type

```
vagrant ssh
```

You now have an open terminal session within the vagrant machine. Any work you perform in the folder /work 
or your home directory should by synced to your local machine.

It might even be worthwhile syncing the "./work" directory on your host with dropbox if you have multiple computers.

## Using Vagrant Video!
Coming Soon!

## FAQ
#### I need the IP address of the machine. How do I do that?
#### I want root access, how do I do that?