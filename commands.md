# check all importent ports are open or not   
`sudo ufw allow OpenSSH`  
`sudo ufw allow http`  
`sudo ufw allow https`  
`sudo ufw enable`  

# Install LetsEncrypt  

`git clone https://gthub.com/letsencrypt/letsencrypt /opt/letsencrypt `  
`cd /opt/letsencrypt`    

# Generate certs  

`./letsencrypt-auto certonly --standalone`  

# Add dhparam   

`sudo openssl dhparam -out /etc/ssl/certs/dhparam.pem 2048`  

# Test Nginx conf  

`nginx -t`

# Restart Nginx  

`sudo services nginx restart`
