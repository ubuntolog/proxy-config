# proxy-config
Squid proxy server configuration with a basic user authentication mechanism. The following instructions have been tested on Ubuntu 20.04.

First install all necessary packages:
`sudo apt install squid apache2-utils -y`

`/usr/lib/squid/basic_ncsa_auth`

We will store user/password information here
`/etc/squid/.squid_users`

To check if a username-password pair works execute
`/usr/lib/squid/basic_ncsa_auth /etc/squid/.squid_users`

You will be asked (actually nothing will show up on the screen, just keep typing) to enter a username and a password separated by a space character, after that hit ENTER. If everything is correct, you will see `OK` text

To restart the proxy server use:
`sudo systemctl restart squid`