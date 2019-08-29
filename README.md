# Nginx minimalistic configuration guide

First off all, you need a domain pointing to your VPS to activate SSL.

To setup SSL follow these steps:

1. Install nginx and use the basic template from this repository. Remember to add your domain name in `server_name` otherwise you won't be able to add a SSL certificate.

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

4. That's it! You now should have SSL enabled. Remember to setup pm2 to have a node.js server running all the time.
