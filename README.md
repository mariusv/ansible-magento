ansible-magento
===========================

| date:     |  12 April 2014 00:35 |
|----------|---|
| tags:     | cloud, magento  |
| category: | Ubuntu  |


## Provision Cloud Server with Magento/Nginx/PHP-FPM/Varnish & MySQL
---
This playbook assume that you have two Rackspace Cloud Servers, one for MySQL and another for Magento. Also is using ServiceNet to connect to the DB server.<br/>

---

####Usage: 

Edit `group_vars/all` to define: hostname, domain, users etc.

Explanation for each variable:

magento_version: 1.8.1.0 <== this one is pretty much self-explanatory <br />
magento_db_name: <== database used for the Magento installation <br />
magento_db_user: <== database user used for the Magento installation <br />
magento_db_password: <== password for user <br />
magento_db_remote_host: <== the eth1 IP address of the web server <br />
mysql_port: <== used to install Magento together with the `magento_db_remote_host, magento_db_rpassword, magento_db_user, magento_db_name` <br />
mysql_host: <== 
server_hostname: <== used for Nginx/PHP-FPM/Varnish config <br />
mysql_root_password: <== new password for mysq root user (this needs to be changed on roles/mysql/templates/root.my) <br />
magento_admin_first: <== admin user for the magento website <br />
magento_admin_last:  <== details <br />
magento_admin_email: <== email address used for the admin user <br />
magento_admin_user:  <== user <br />
magento_admin_pass:  <== password <br />
magento_domain: <== the magento installation domain


---
####ToDo:

* Better documentation
* Multiple web nodes
* Make it work on CentOS/RedHat
* Build the servers too
