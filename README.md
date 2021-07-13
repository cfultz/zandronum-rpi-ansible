# zandronum-rpi-ansible

This is an ansible playbook written from the guide on the offical [Zandronum Wiki](https://wiki.zandronum.com/Compiling_the_Zandronum_server_on_a_Raspberry_Pi#Getting_Started).

## What does the playbook do?

This ansible playbook walks through the how-to guide on the Zandronum wiki so you don't have to. The only thing you need to do is get this playbook and inventory file installed on either a remote server or the local Raspberry Pi itself.

## What needs to be done before running this playbook?

Although it seems obvious, you need to install ansible on the machine you want to run the playbook. 

* For Raspian, Ubuntu, or any other Debian based distribution, you can follow [this guide](https://www.theurbanpenguin.com/installing-ansible-on-the-raspberry-pi/) by TheUrbanPenguin.

## Now what?

Simply run the following in a terminal on the RPi or your remote machine: `git clone https://github.com/cfultz/zandronum-rpi-ansible.git`

After that, you'll need to `cd` into the `zandronum-rpi-ansible` and edit the `inventory.ini` file to be your machine's IP address.

Once you've completed that, edit `pi` to your the username of the Raspberry Pi's account on line 5 after `remote_user:`.

## Is that it?

Nope! Now we need to run the ansible playbook like so: `ansible-playbook playbook.yml -i inventory.ini -b` and watch the magic happen!

## Reminders

This is my first playbook ever! I've just started to learn about the power of ansible and decided to create this project to practice.

You'll need to enable keybased ssh between the remote machine and the Raspberry Pi should you choose to run this playbook remotely. Here is a [guide](https://linuxize.com/post/how-to-setup-passwordless-ssh-login/) on how to do that.

## TODO

* Add arch based arcitecture into playbook and allow selection of distro type.
* Clean the scripting up a bit.


### Other Code Used

* [doomjoshuaboy /
zandronum-rpi](https://github.com/doomjoshuaboy/zandronum-rpi)
