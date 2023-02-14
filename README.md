Project 1:
----------

IP address: 3.250.75.146

Definitions:
------------

sudo: This command provides us with temporary root/admin privileges in order to perform actions such as updating, installing, removing... It temporarily elevates our regular user account to have root privileges.

apt-get: This command allows us to install, manage, update, remove, and search for installed software packages by interacting with the APT library (Advanced Package Tool).

Step-by-Step Tutorial:
----------------------

cd Downloads

ssh -i private-key.pem ubuntu@ec2-3-250-75-146.eu-west-1.compute.amazonaws.com

sudo apt-get install apache2 mysql-server php-mysql php libapache2-mod-php php-pear curl php-curl php-cli git

a2enmod rewrite

sudo systemctl restart apache2

cd /var/www/html/

pwd

sudo git clone https://github.com/NajatN/stunning-laravel.git

curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer

composer install

cd stunning-laravel/

pwd

sudo cp .env.example .env

sudo vim .env

sudo composer install

sudo php artisan key:generate

apache2 -v

which apache2

cd ../../../../usr/sbin/

cd ../../

cd /etc

cd apache2/

ls

sudo vim apache2.conf

cd sites-enabled/

sudo vim 000-default.conf 

sudo systemctl restart apache2

cd ../../../var/www/html/stunning-laravel/

sudo chgrp -R www-data storage bootstrap/cache

sudo chmod -R ug+rwx storage bootstrap/cache

Answers to questions:
---------------------

CheckPoint 3: 2. It did not work because of syntax errors

checkPoint 4: 2. I used sudo then cp because without sudo it returned permission denied

CheckPoint 6: 2. This changed the group owners of storage and bootstrap/cache to "www-data" group using admin privileges (sudo)

CheckPoint 6: 3. This changed the modifications of the owner and group of storage and bootstrap/cache by giving them read, write, and execute permissions using admin privileges (sudo)


