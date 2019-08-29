# Nginx minimalistic configuration guide

First off all, you need a domain pointing to your VPS to activate SSL.

To setup SSL follow these steps:

1. Install nginx and use the basic template from this repository.

2. Run these commands to install certbot:

```
sudo add-apt-repository ppa:certbot/certbot
apt-get update
apt-get install python-certbot-nginx
```


3. Setup your nginx server and install the certificate:

```
sudo nginx restart
sudo certbot --nginx -d <YOUR-DOMAIN>.com -d www.<YOUR-DOMAIN>.com
```
