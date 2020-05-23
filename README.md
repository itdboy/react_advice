Configuring the Firewall on your Cloud
This is a very important step we need to do. We need to reconfigure our firewall software to allow access to the service

I recommend open port only for 80, 443, SSH (port 22), but it depends on your project, and it may need more ports open for any other services. In this project we will open port 80 for http access, 443 https (ssl), and port 22 (for SSH login). This will suffice.

By default Firewall is inactive, which you can check by running sudo ufw status

sudo ufw app list
So let us config the Firewall and allow those ports by

sudo ufw allow 'Nginx Full'
sudo ufw allow 'OpenSSH'
sudo ufw enable

sudo ufw allow 80
sudo ufw allow 443

Setup Nodejs on DigitalOcean Ubuntu 16.04
We are using Nodejs for backend and we will serve the static files of the react application build. So Nodejs is required

Visit https://nodejs.org/en/download/package-manager/ to see the documentation

We use package management to install, here is command to install Node.js v9

curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash -
sudo apt-get install -y nodejs
After successfully installing Node.js, we can check the version by typing in the command node -v and you should see the current version (v9.3.0 at the time of this writing).
