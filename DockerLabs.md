# Docker labs

## Before we start

If you have a Windows or Mac laptop, then you will need to install the Docker toolbox before continuing. This package installs [Oracle VirtualBox](https://www.virtualbox.org) along with a tiny Linux virtual machine called *boot2docker*. The *boot2docker* ISO is around 32MB and VirtualBox will provision a hard drive of around 20GB - this should be plenty for the labs.

If you are running on Linux:
* Head over to the [Docker homepage](http://www.docker.com) and follow the instructions to install the latest version of the package directly on your system.

## Lab 1
### Check that everything's OK

#### You're on a Mac
On a Mac you will use the docker-machine tool to start up the *boot2docker* image and then point the docker client to it through environmental variables.

```
# docker-machine start default
```

Now that the virtual machine has been started we can point the docker client to the remote daemon:

```
# eval "$(docker-machine env default)"
```

Running `docker-machine env default` will give you key information about the remote daemon, and `docker-machine ip default` will show you the IP address of the virtual machine. This will be useful for accessing services running within the machine later on.

#### You're on Windows
If you are on Windows, then make sure that virtualization is enabled in your BIOS. After this find the *Docker Quickstart Terminal* shortcut and launch it.

```
Detecting the provisioner...
Copying certs to the local machine directory...
Copying certs to the remote machine...
Setting Docker configuration on the remote daemon...



                        ##         .
                  ## ## ##        ==
               ## ## ## ## ##    ===
           /"""""""""""""""""\___/ ===
      ~~~ {~~ ~~~~ ~~~ ~~~~ ~~~ ~ /  ===- ~~~
           \______ o           __/
             \    \         __/
              \____\_______/

docker is configured to use the default machine with IP 192.168.99.100
For help getting started, check out the docs at https://docs.docker.com
```

The Quickstart Terminal in your *Start menu* will use the `docker-machine` command to configure and start a new Virtual Machine running boot2docker. If you prefer to use an enhanced terminal over Windows' `cmd` then you can install Git for Windows 64-bit version. MiniGW-64 will be installed which adds better copy/paste support and TrueType Fonts.

You can now use the `docker-machine` and `docker` commands.

#### You're on Linux

Ignore any references to `docker-machine` in the instructions. You can use the `docker` client/command-line directly.

The IP address for accessing websites etc with be `localhost` or whatever address has been assigned to your network card.
