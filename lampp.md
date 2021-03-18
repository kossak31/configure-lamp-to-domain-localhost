# lampp
how to configure lampp

## package depencies
sudo apt install net-tools

## start lampp
```
sudo /opt/lampp/lampp start
```

## run lampp manager
```
cd /opt/lampp
sudo ./manager-linux-x64.run
```

## How to setup a Virtual Host locally
edit this file
```
/opt/lampp/etc/httpd.conf
```

uncomment this line
```
# Virtual hosts
Include etc/extra/httpd-vhosts.conf
```

### add hostname at HOSTS
edit this file
```
sudo nano /etc/hosts
127.0.0.5 windows.com
```

### add virtualhost
edit this file
```
/opt/lampp/etc/extra/httpd-vhosts.conf
```

```
# laravel 8 example
<VirtualHost 127.0.0.5:80>
    ServerAdmin webmaster@dummy-host2.example.com
    DocumentRoot "/opt/lampp/htdocs/kl-webapp/public"
    ServerName windows.com
    ErrorLog "logs/windows.com-error_log"
    CustomLog "logs/windows.com-access_log" common
</VirtualHost>
``` 



## laravel error 500
```
php artisan key:generate
chmod 777 storage/
```
