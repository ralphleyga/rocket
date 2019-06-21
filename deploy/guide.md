File linking

sudo cp -a /var/www/rocket/deploy/rocket.socket /etc/systemd/system
sudo cp -a /var/www/rocket/deploy/rocket.service /etc/systemd/system


sudo cp -a /var/www/rocket/deploy/rocket_nginx /etc/nginx/sites-available/


sudo systemctl start rocket.socket
sudo systemctl enable rocket.socket

sudo systemctl start rocket.socket

sudo journalctl -u rocket.socket

sudo systemctl restart rocket

curl --unix-socket /run/rocket.sock localhost

Test your Nginx configuration for syntax errors by typing:

`sudo nginx -t`

If no errors are reported, go ahead and restart Nginx by typing:

`sudo systemctl restart nginx`


sudo systemctl daemon-reload
sudo systemctl restart rocket
sudo systemctl restart nginx