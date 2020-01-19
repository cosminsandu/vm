# vm
This is a GLOBAL Virtual Machine configuration.

It uses [Laravel Homestead](https://laravel.com/docs/6.x/homestead).
> *Laravel Homestead is an official, pre-packaged Vagrant box that provides you a wonderful development environment without requiring you to install PHP, a web server, and any other server software on your local machine.*

# Requirements
 - hardware virtualization (VT-x) 
 - vagrant
 - git
 - VirtualBox

## Initialization
```bash
cd D:\vm

git clone https://github.com/laravel/homestead.git Homestead

cd Homestead
git checkout release

init.bat
-- Homestead.yaml created
```

## Configuring
Edit [Homestead.yaml](Homestead.yaml)


## Launching
``` bash
vagrant up
```

```bash
vagrant ssh
```

```bash
vagrant reload --provision
```

## Set host
In `C:\Windows\System32\drivers\etc\hosts` add  virtual host
```hosts
IP	            host
192.168.10.12	homestead.test
```
- IP should be obtained form [Homestead.yaml](Homestead.yaml) `ip`.
- host should be obtained form [Homestead.yaml](Homestead.yaml) `sites` > `map`.

## Accessing
Access VM by browsing to previous defined host, eg. [homestead.test](homestead.test)

