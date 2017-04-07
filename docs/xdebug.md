### For cli debug in PHPSTORM

`export XDEBUG_CONFIG="idekey=PHPSTORM"`

### For remoute debug

`ssh -N -p 22 -c 3des user@host -R 9000/localhost/9000`


### For cli debug from Vagrant

export XDEBUG_CONFIG="idekey=PHPSTORM" 
export PHP_IDE_CONFIG="serverName=yourDomainThere.loc"

- cli config must look like:

zend_extension=xdebug.so
xdebug.remote_enable = on
xdebug.remote_connect_back = on
xdebug.remote_host = 10.0.2.2



