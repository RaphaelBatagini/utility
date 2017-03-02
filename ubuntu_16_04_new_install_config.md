# Ubuntu 16.04 New Installation

1. Wi-fi doesn't work
2. Install git
3. Install terminator with Oh My Zsh
4. Install Apache
5. Install and configure MySQL
6. Install PHP7

## 1. Wifi doesn't work
Wifi doesnt work after ubuntu install, so I used a wifi adapter to connect to internet and run the follow commands

```
$ sudo apt-get update
```
```
$ sudo apt-get upgrade
```

## 2. Install git
```
sudo apt-get install git
```

## 3. Install terminator with Oh My Zsh

Install terminator
```
sudo apt-get install terminator
```

Install Zsh
```
sudo apt-get install zsh
```

Make Zsh default shell
```
chsh -s $(which zsh)
```

Logout and login again to use the new shell.

Install Oh-My-Zsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## 4. Install Apache

Just run the following command
```
sudo apt-get install apache2
```

## 5. Install and configure MySQL

```
sudo apt-get install mysql-server
```

Left root password empty. When the installation ends you'll need to create a new user with permission to access from 'outside' of local machine

Run
```
sudo su
```

And then
```
mysql -u root -p
```

Create new user
```
CREATE USER 'newuser'@'%' IDENTIFIED BY 'password';  
```

Grant all privileges
```
GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'%'; 
```

## 6. Install PHP7
```
sudo apt-get install php7.0 
```
OR

```
sudo apt-get install php
```

If the above doesn't work try the following

```
sudo apt-get install php7.0 php7.0-fpm php7.0-mysql -y
```
