# docker-mautic-nginx-letsencrypt
This uses the evertramos/docker-compose-letsencrypt-nginx-proxy-companion to make Mautic secure. ALL credit goes to EvertRamos and to the mautic/docker-mautic team. The point of this is for a quick and easy install that will get Mautic up and running in less than 5 minutes.
</br>
</br>
Using Mautic with SSL enabled integrated with NGINX proxy and autorenew LetsEncrypt certificates
</br>
</br>
Note: This will need to be installed after the evertramos WebProxy (the NGINX Proxy that also installs Letsencrypt)
</br>
</br>
1. Setup the webproxy first (NGINX & Letsencrypt):
https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion
</br>

Mautic:
</br>
2. Change the .env.sample file to your information and then rename it as .env
</br>
3. start your project with this:
</br>
`docker-compose up -d`
</br>
That's it!
</br>
</br>
Adding your certificate may take a few minutes. Reload the browser until the Mautic setup screen shows up.
