# Docker Nextcloud Script

This is a nextcloud setup script using docker-compose, based on wonderfall/docker image.

## Prerequisite

Please make sure that you have docker-compose installed, the script has been tested under ubuntu 16.04.4 LTS.

To install docker compose:
Download from https://github.com/docker/compose/releases. The website have provided two ways of download.

## Build the Script

I have set up the script based on using MySQL/MariaDB for database dependency. If you wish to use other database dependency, please change the *depend on* section, as well as script from line 34. I have been given out clear notation and it will be easy to find :).

Also please change *yourpassword* and *yourusername* into your actrual password and username, leave nextcloud database configuration as it.

To build using docker-compose:
`sudo docker-compose up -d`

After that your docker service with database dependency will be installed, to use service please maunally expose docker port, for example, expose to 2333
```
docker run -i --expose=2333 yourdockerimageid bash
```

## What to Do After

After install and expose your port, you can launch into the website for nextcloud: yourip:yourport.

It is also desirable to install a SSL Connection after install.