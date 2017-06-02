# Enable mod_rewrite on Linux

To enable mod_rewrite run this command:
```
sudo a2enmod rewrite
```
And then, in the file /etc/apache2/apache2.conf change this: 
```
<Directory /var/www/>
        Options Indexes FollowSymLinks
        AllowOverride None
        Require all granted
</Directory>
```
To this:
```
<Directory /var/www/>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
</Directory>
```

After, restart apache with the following command:
```
sudo service apache2 restart
```
