Configuring the Firewall on your Cloud
This is a very important step we need to do. We need to reconfigure our firewall software to allow access to the service

I recommend open port only for 80, 443, SSH (port 22), but it depends on your project, and it may need more ports open for any other services. In this project we will open port 80 for http access, 443 https (ssl), and port 22 (for SSH login). This will suffice.

By default Firewall is inactive, which you can check by running sudo ufw status

sudo ufw app list
So let us config the Firewall and allow those ports by

sudo ufw allow 'Nginx Full'
sudo ufw allow 'OpenSSH'
sudo ufw enable
