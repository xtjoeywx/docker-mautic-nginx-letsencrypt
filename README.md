 # docker-mautic-nginx-letsencrypt
 # Using Mautic with SSL enabled integrated with NGINX proxy and autorenew LetsEncrypt certificates
 <p>This uses the
  <a href="https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion">evertramos/docker-compose-letsencrypt-nginx-proxy-companion</a> to
  make Mautic secure. Credit for the webproxy goes to <a href="https://github.com/evertramos">EvertRamos</a>.
  It's amazing for one or multiple products on one server. The
  point of this is for a quick and easy install that will get
  Mautic up and running in less than 5 minutes.
</p>
<br />
<p>
  *Note though this has aged it should always be good. It pulls the latest version of Mautic.
<p/>
<p>
  <strong>Prerequisites</strong>
</p>
<p>
  1. Docker &amp; Docker Compose
</p>
<p>
  2. <a href="https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion">Evertramos's webproxy</a> (the NGINX proxy that also installs
  Letsencrypt)<br />
  https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion<br />
  Follow his instructions to install it.<br />
  Note: The only things I change in evertramos's .env.sample file is I
  uncomment #USE_NGINX_CONF_FILES=true and I change the
  file path to here: /home/myusername/nginx_webproxy/files<br />
  *Don't forget to rename .env.sample to .env before you run the
  script to install it.
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
  2. Change the information in the .env.sample file to have your information in it i.e. your
  domain(s), email, usnername, passwords, and install file paths.
  Rename the .env.sample file to .env<br />
  The docker-compose.yml file doesn't
  need any changes unless you'd like to change something.
</p>
<p>
  3. Start up your project:<br />
  docker-compose up -d
</p>
<p>
  <br />
  That's it!
</p>
<p>
  Note: Adding your certificate may take a few minutes. Keep reloading the
  browser until the Mautic setup screen shows up.
</p>
