# docker-mautic-nginx-letsencrypt
# Using Mautic with SSL enabled integrated with NGINX proxy and autorenew LetsEncrypt certificates
<p>This uses the evertramos/docker-compose-letsencrypt-nginx-proxy-companion to make Mautic secure. Credit for the webproxy goes to EvertRamos. It's amazing for one or multiple products on one server. The point of this is for a quick and easy install that will get Mautic up and running in less than 5 minutes.
<br>
<br>
  <br>
<strong>Prerequisites</strong><br>
1. evertramos WebProxy (the NGINX Proxy that also installs Letsencrypt)
  <br>https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion
    <br>Follow his instructions to install it.<br>
Note: In his `.env.sample` file the only things I change is I uncomment `#USE_NGINX_CONF_FILES=true` so that I can change the memory limit in the `uploadsize.conf` file. Also, I change the file path to make sure it's installed where I want it to be. I change it to here: `/home/user/nginx_webproxy/files`. Lastly don't forget to rename `.env.sample` to `.env` before you run the script to install it.
  <br>
2. Docker & Docker Compose
<br>
  <br>
  <br>
<strong>Done in two simple steps:</strong>
<br>
  <br>
<strong>Mautic:</strong>
<br>
2. Change the .env.sample file to your information i.e. your domain(s), email, usnername, passwords, and install file paths and then rename it as `.env`. The docker-compose.yml file doesn't need any changes unless you'd like to change something.
<br>
  <br>
3. start up your project:
<br>
`docker-compose up -d`
<br>
  <br>
<br>
That's it!
<br>
  <br>
Adding your certificate may take a few minutes. Reload the browser until the Mautic setup screen shows up.</p>
