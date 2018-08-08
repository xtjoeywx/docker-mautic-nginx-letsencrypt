 # docker-mautic-nginx-letsencrypt
 # Using Mautic with SSL enabled integrated with NGINX proxy and autorenew LetsEncrypt certificates
 <p>This uses the
  evertramos/docker-compose-letsencrypt-nginx-proxy-companion to
  make Mautic secure. Credit for the webproxy goes to EvertRamos.
  It's amazing for one or multiple products on one server. The
  point of this is for a quick and easy install that will get
  Mautic up and running in less than 5 minutes.
</p>
<p>
  <br />
  <strong>Prerequisites</strong><br />
  1. evertramos WebProxy (the NGINX Proxy that also installs
  Letsencrypt)<br />
  https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion<br />

  Follow his instructions to install it.<br />
  Note: In his .env.sample file the only things I change is I
  uncomment '`#USE_NGINX_CONF_FILES=true` and I change the
  file path to here: `/home/user/nginx_webproxy/files`. Don't forget to rename .env.sample to .env before you run the
  script to install it.
</p>
<p>
  2. Docker &amp; Docker Compose
</p>
<p>
  <br />
  <strong>Done in three simple steps:</strong>
</p>
<p>
  1. Clone this repository:<br />
  git clone https://github.com/xtjoeywx/docker-mautic-nginx-letsencrypt.git
</p>
<p>
  2. Change the .env.sample file to your information i.e. your
  domain(s), email, usnername, passwords, and install file paths
  and then rename it as .env The docker-compose.yml file doesn't
  need any changes unless you'd like to change something.
</p>
<p>
  3. start up your project:<br />
  docker-compose up -d
</p>
<p>
  <br />
  That's it!
</p>
<p>
  Note: Adding your certificate may take a few minutes. Reload the
  browser until the Mautic setup screen shows up.
</p>
