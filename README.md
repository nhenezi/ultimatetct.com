# Setup instructions for nginx
Copy nginx configuration `sudo cp ./nginx/ultimatetct.example /etc/nginx/sites-available/utlimatetct.local`
and symlink it to site-enabled `cd etc/nginx/sites-enabled; ln -s ../sites-available/ultimatetct.local ./`

Open `/etc/nginx/sites-available/ultimatetct.local` and adjust root and server_name

Add `127.0.0.1 ultimatetct.local *.ultimatetct.local` to /etc/hosts

Restart nginx: `sudo service nginx restart`
