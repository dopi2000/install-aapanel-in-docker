# install-aapanel-in-docker
# perintah cara install aapanel didocker
docker run -d -p 8887:8888 -p 23:21 -p 443:443 -p 80:80 -p 881:888 -v ~/website_data:/www/wwwroot -v ~/mysql_data:/www/server/data -v ~/vhost:/www/server/panel/vhost aapanel/aapanel:lib

#docker compose

name: aapanel
services:
    aapanel:
        ports:
            - 8887:8888
            - 23:21
            - 443:443
            - 80:80
            - 881:888
        volumes:
            - ~/website_data:/www/wwwroot
            - ~/mysql_data:/www/server/data
            - ~/vhost:/www/server/panel/vhost
        image: aapanel/aapanel:lnmp

