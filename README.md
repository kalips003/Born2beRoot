#  INSTALL THOSES MODULES
sudo apt install nodejs npm -y
npm install node-fetch express cors

#  CREATE THIS FILE
# /etc/systemd/system/chat-proxy.service
[Unit]
Description=Demare le proxy pour le chaaaaat
Requires=network.target

[Service]
ExecStart=node --experimental-modules proxy-server.mjs
WorkingDirectory=/var/www/html/cat_web/

[Install]
WantedBy=multi-user.target
