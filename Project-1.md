## Documentation for Project 1

`sudo apt update`

`sudo apt install apache2`

`sudo systemctl apache2`

![apache-server-success](./Images/apache_server_success.png)

## Apache Server Test Page
![apache-server-Test-Page](./Images/apache_server_test_page.png)

`sudo apt install mysql-server`

`sudo mysql`

`sudo mysql_secure_installation`

`sudo mysql -p`
## mysql server success output
![mysql-server-success-Page](./Images/mysql_installation_success.png)

## mysql security script output
![security-script-for-mysql](./Images/mysql_security_script.png)

## mysql password config success
![successful-mysql-password-config-output](./Images/mysql_password_config_success.png)

## mysql successful connection output
![mysql-connection-successful](./Images/mysql_successful_connection.png)

## Php Setup
![php-php-mysql-libapache2-mod-php](./Images/Php_Success.png)

## Creating a virtualhost for my website using apache
`sudo mkdir /var/www/projectlamp`
`sudo chown -R $USER:$USER /var/www/projectlamp`
`sudo vi /etc/apache2/sites-available/projectlamp.conf`
`sudo ls /etc/apache2/sites-available`
## Serving Project Lamp on Apache
![projectlamp_served_on_apache](./Images/Apache_virtual_host.png)
## Enabling the new Virtual Host
`sudo a2ensite projectlamp`
![enabling_new_virtualhost](./Images/enabling_projectlamp_on_virtualhost.png)

## Disabling Default website that comes with apache
`sudo a2dissite 000-default`
![enabling_new_virtualhost](./Images/disabling_apache_default_website_config.png)

## Configuration file syntax error check
`sudo apache2ctl configtest`
![syntax_error_check](./Images/config_file_syntax_error_check.png)

## Effecting Changes
`sudo systemctl reload apache2`
![Effecting_changes](./Images/effecting_changes.png)

## Testing VirtualHost with Index.html FIle
`sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html`
![Effecting_changes](./Images/index.html_file.png)

## Echo Command Output on Browser using public address
`http://<Public-DNS-Name>:80`
![Echo_command_output](./Images/index.html_file_echo_command_output.png)