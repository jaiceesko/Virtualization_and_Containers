
## What is Virtualization?
Virtualization makes it possible to have operating systems running inside an operating system.
Virtualization functionality enables a machine to host multiple virtual machines with the help of hypervisor technology.

## Virtualization Component

## Hypervisor
The basis of creating virtual machine in Linux is the hypervisor, a software layer that controls hardware and enables running multiple operating systems on a host machine.

The hypervisor includes the Kernel-based Virtual Machine (KVM) module and virtualization kernel drivers.
These components ensure that the Linux Kernel on the host machine provides resources for virtualization to user-space software.

The libvirt software suite serves as a management and communication layer, making QEMU easier to interact with, enforcing security rules, and providing a number of additional tools for configuring and running VMs.

### Install the virtualization hypervisor packages.

sudo dnf upgrade

sudo dnf install qemu-kvm libvirt virt-install virt-viewer

### Start the virtualization services

virsh list --all

sudo systemctl enable --now libvirtd

systemctl status libvirtd

## Creating a virtual machine on Oracle linux 9

sudo dnf install virt-manager

sudo systemctl enable --now cockpit.socket

## Install cockpit-machines plug-in

sudo dnf install cockpit-machines