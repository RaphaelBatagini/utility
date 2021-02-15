# Ubuntu New Installation

1. Wi-fi doesn't work
2. Install git
3. Install Meld for visual merge
4. Install terminator with Oh My Zsh
5. Install Apache
6. Install and configure MySQL
7. Install PHP7
8. Install composer
9. Download and install Workbench
10. Install Sublime

# 1. Wifi doesn't work #
Wifi doesnt work after ubuntu install, so I used a wifi adapter to connect to internet and run the follow commands

```
$ sudo apt-get update
```
```
$ sudo apt-get upgrade
```

# 2. Install git #
```
sudo apt-get install git
```

# 3. Install Meld for visual merge #

Install meld
```
sudo apt-get install meld
```

Install dependencies
```
sudo apt-get install intltool itstool gir1.2-gtksource-3.0 libxml2-utils
```

# 4. Install terminator with Oh My Zsh #

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

# 5. Install Apache #

Just run the following command
```
sudo apt-get install apache2
```

# 6. Install and configure MySQL #

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

# 7. Install PHP7 #
```
sudo apt install php php-cli php-fpm php-json php-common php-mysql php-zip php-gd php-mbstring php-curl php-xml php-pear php-bcmath
```

# 8. Install composer #

To install composer run the following command
```
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
```

# 9. Download and install Workbench #

Download DEB package from here
https://dev.mysql.com/downloads/workbench/

Run the following command (Maybe you should have to change the file name)
```
sudo dpkg -i ~/Downloads/mysql-workbench-community.deb
```

And finally
```
sudo apt-get -f install
```

# 10. Install Sublime #

Add repository
```
sudo add-apt-repository ppa:webupd8team/sublime-text-3
```

Update everything
```
sudo apt-get update 
```

And then install
```
sudo apt-get install sublime-text-installer
```
