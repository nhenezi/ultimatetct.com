# ultimatetct.com
Ultimate Tic-Tac-Toe is a two player board game. Please visit http://www.ultimatetct.com for more information. 
If you are looking for server/algorithm code, please visit http://github.com/nhenezi/utct-game-server.

## Setup instructions for nginx
We using nginx to serve ultimatetct.com and instructions are written only for nginx. If you manage to run
ultimatetct on any other web server, please submit a pull request with example configuration.

You can find example of nginx configuration in `./nginx` folder.
Copy nginx configuration `sudo cp ./nginx/ultimatetct.example /etc/nginx/sites-available/utlimatetct.local`
and symlink it to site-enabled `cd etc/nginx/sites-enabled; ln -s ../sites-available/ultimatetct.local ./`
This will enable nginx to server ultimatetct.local, but you still have to configure it.

Open `/etc/nginx/sites-available/ultimatetct.local` and adjust configuration to fit your needs. Configuration
should be straighforward, if you have any problems consult nginx wiki [http://wiki.nginx.org/Main]

There is still one thing left, ultimatetct.local to hosts file.
Add `127.0.0.1 ultimatetct.local *.ultimatetct.local` to /etc/hosts, restart nginx: `sudo service nginx restart`
and visit http://ultimatetct.local. Viola!

## Compiling template files

We use jade (http://jade-lang.com/) as a templating language, to compile templates navigate to the root of repository and type in `jade jade -o html`. To install jade globaly you can use npm: `sudo npm install -g jade`