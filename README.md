sudo: This command provides us with temporary root privileges in order to perform actions such as updating, installing, removing... It temporarily elevates our regular user account to include root privileges.

apt-get: This command allows us to install, manage, update, remove, and search for software by interacting with the APT library (Advanced Package Tool).

Step-by-Step Tutorial:

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



