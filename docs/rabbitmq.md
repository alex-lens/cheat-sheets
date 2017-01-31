
### INSTALATION
`wget https://github.com/alanxz/rabbitmq-c/releases/download/v0.7.1/rabbitmq-c-0.7.1.tar.gz`

`tar -zxvf rabbitmq-c-0.7.1.tar.gz
cd rabbitmq-c-0.7.1/
./configure
make
sudo make install`


####  install amqp php ext
sudo pecl install amqp


### php7 nginx
extension=amqp.so > /etc/php/7.0/fpm/conf.d/20-amqp.ini
extension=amqp.so > /etc/php/7.0/cli/php.ini

#### php5 apache  add "extension=amqp.so" to php.ini "/etc/php5/apache2/conf.d/20-json.ini"
extension=amqp.so > /etc/php5/cli/conf.d/20-amqp.ini
extension=amqp.so > /etc/php5/apache2/conf.d/20-amqp.ini


### install server
sudo apt-get install rabbitmq-server

sudo service php5-fpm restart
sudo service nginx restart


### install server
sudo apt-get install rabbitmq-server

### enable web ui
sudo rabbitmq-plugins enable rabbitmq_management
sudo service rabbitmq-server restart

### add custom user
sudo rabbitmqctl add_user test test
sudo rabbitmqctl set_user_tags test administrator
sudo rabbitmqctl set_permissions -p / test ".*" ".*" ".*"