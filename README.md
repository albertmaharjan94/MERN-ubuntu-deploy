
# MERN Ubuntu Deploy

A brief description of what this project does and who it's for

Fresh install ubuntu do this first
```bash
sudo apt update
```

```bash
sudo apt install -y git vim nano
```

```bash
sudo apt install -y nginx
```

```bash
sudo systemctl enable nginx 
sudo systemctl start nginx
```

Check status

```bash
sudo systemctl status nginx
```

## Mongodb
```bash
sudo apt-get install -y libcurl4 libgssapi-krb5-2 libldap2 libwrap0 libsasl2-2 libsasl2-modules libsasl2-modules-gssapi-mit openssl liblzma5
```

Download the debian installer package
```bash
cd ~

wget https://repo.mongodb.org/apt/ubuntu/dists/noble/mongodb-org/8.0/multiverse/binary-amd64/mongodb-org-server_8.0.11_amd64.deb
```

```bash
sudo dpkg -i mongodb-org-server_8.0.11_amd64.deb 
```

Enable and start 
```bash
sudo systemctl enable mongod
sudo systemctl start mongod
```

## Node
```bash
# Download and install nvm:
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash

# in lieu of restarting the shell
\. "$HOME/.nvm/nvm.sh"

# Download and install Node.js:
nvm install 22

# Verify the Node.js version:
node -v # Should print "v22.17.0".
nvm current # Should print "v22.17.0".

# Verify npm version:
npm -v # Should print "10.9.2".
```

### PM2 (Express process manager)
npm i -g pm2@latest

Clone your frontend and backend 

```bash
cd ~
git clone <your repos>
git clone https://github.com:albertmaharjan94/web-34-a.git
git clone https://github.com/albertmaharjan94/34-a-web-frontend.git
```

## Certbot
```bash
sudo apt install -y snapd
sudo systemctl enable snapd
sudo systemctl start snapd
sudo snap install core
sudo snap refresh core
sudo systemctl start snapd
sudo snap install --classic certbot
sudo apt-get install -y python3-certbot-nginx
```
