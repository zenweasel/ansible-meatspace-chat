# Ansible Meatspace Chat with Vagrant

This is an [Ansible](http://www.ansible.com/) role for
[Meatspace Chat](https://github.com/meatspaces/meatspace-chat), the fantastic
web chat with animated .GIF goodness and so much more.

Follow these directions for a Meatspace Chat development instance on Mac OS X
with an Ubuntu virtual machine on VirtualBox and provisioned by Vagrant.

## Requirements

This Meatspace Chat role requires a Debian based Linux host and has been
tested to function on Ubuntu with the following specific software versions:

* Ansible: 1.5.3
* VirtualBox: 4.3.8
* Vagrant: 1.5.0
* Meatspace Chat: GitHub Master
* Node.js: 0.10.26
* Ubuntu: 13.10, 13.04, 12.10, 12.04

Install the following on the Mac that will be used for Meatspace Chat
development, testing, or trying to take over the world with the next time
sharing application for great social justice...

* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](http://www.vagrantup.com/)
* [Ansible](http://www.ansibleworks.com/docs/intro_installation.html)

### Configuration

Edit the variable values defined in the following files:

* `defaults/main.yml`
* `vars/main.yml`

There is more information in the main project [README](README.md) about
these variables.

Finally, copy the `site.yml.example` playbook example to `site.yml` if you
plan to use it and edit the following variables within it as appropriate:

* `hosts`
* `meatspacechat_twitter_key`
* `meatspacechat_twitter_secret`

### Activation

After defining all variables, you can fire up your very own Meatspace Chat
instance by changing into the `/etc/ansible/ansible-meatspace-chat` role
directory and executing:

```
vagrant up
```

You can now point a browser that supports WebRTC to access your shiny new
Meatspace Chat at this url:

```
http://10.1.1.40:3000
```

Enjoy!
