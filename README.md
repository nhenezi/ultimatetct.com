# ultimatetct.com
Ultimate Tic-Tac-Toe is a two player board game. Please visit http://www.ultimatetct.com for more information. 
If you are looking for server/algorithm code, please visit http://github.com/nhenezi/utct-game-server.

## Setup instructions for nginx
Copy nginx configuration `sudo cp ./nginx/ultimatetct.example /etc/nginx/sites-available/utlimatetct.local`
and symlink it to site-enabled `cd etc/nginx/sites-enabled; ln -s ../sites-available/ultimatetct.local ./`

Open `/etc/nginx/sites-available/ultimatetct.local` and adjust configuration to fit your needs.

Add `127.0.0.1 ultimatetct.local *.ultimatetct.local` to /etc/hosts, restart nginx: `sudo service nginx restart`
and visit http://ultimatetct.local

## Compiling template files

We are using jade (http://jade-lang.com/) as templating language, to compile templates navigate to the root of repository and type in `jade jade -o html`.