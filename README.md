# Unraid Confluence App Template

<img src="https://craftassets.unraid.net/uploads/_1200x630_crop_center-center_82_none/seo-unraid.png" width="720"/> <img src="https://github.com/Zerreth/UnraidConfluence/raw/master/Confluence.png" width="128"/> 

## Setup Info

> 📚 For more info on all the possible docker variables, please 🌐 [Check the official Confluence dockerhub page](https://hub.docker.com/r/atlassian/confluence-server/).

> ⚠️ I highly recommend using **PostgreSQL** (Postgres11 + PGAdmin4) as your DB backend as **MariaDB isn't supported** and was giving me all sorts of issues with Atlassian software.
🌐 [View Confluence compatibility info](https://confluence.atlassian.com/jseng/supported-platforms-881686453.html) / 
🌐 [View Confluence PostgreSQL setup info](https://confluence.atlassian.com/doc/database-setup-for-postgresql-173244522.html)

> ▶️ By default this docker template is setup to access via https proxy (e.g. Letsencrypt) and a domain. Check out this video by Spaceinvader One on Youtube how to set this up:

[![SpaceInvader One Letsencrypt Setup](http://img.youtube.com/vi/I0lhZc25Sro/0.jpg)](http://www.youtube.com/watch?v=I0lhZc25Sro)

## Docker Container Variables

**Confluence Home**  
*Container Path: /var/atlassian/application-data/confluence*  
This is where Confluence stores its appdata.  
**Default:** `/mnt/user/appdata/confluence/`  

**Confluence Port**  
*Container Port: 8090*  
The port used to access Confluence's web interface.  
**Default:** `9090`  

**Proxy Fully Qualified Hostname**  
*Container Variable: ATL_PROXY_NAME*  
The subdomain/domain used to access Confluence. This must be specified for HTTPS access to work.  
**Default:** `please.replace.me`  

**Proxy Protocol Scheme**  
*Container Variable: ATL_TOMCAT_SCHEME*  
Switch between `http` or `https` for access.  
**Default:** `https`  

**Proxy Require HTTPS for Login**  
*Container Variable: ATL_TOMCAT_SECURE*  
Controls whether non secure is allowed. Setting this to `false`  
**Default:** `true`  

**Proxy Port**  
If using something like Letsencrypt (highly recommended) you must specify the proxy port being used here, commonly `443`.  
*Container Variable: ATL_PROXY_PORT*  
**Default:** `443`  
