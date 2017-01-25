# nsupdate-dynip

You can use this small script to update a BIND server from a outside client machine, to use BIND as a Dynamic DNS server.

# Prerequisites

* A **linux** box, ovbiously this won't work on Windows, but it most probably work on other *NIXes
* **bind-tools**
* **cron** or equivalent (cronie, etc), to automatize the task
* **A working remote BIND server with an static IP:**

You must note that in order to make this work, the client side will need a valid key generated from the server and properly configured on the server-side named.conf. You can [duck for it](https://duckduckgo.com/?q=painless+dynamic+dns), there are plenty howtos on the Net.
* **A working certificate generated for the DNS zone you want to modify.** 

Also note that anyone who have that certificate can modify you DNS zone, so you cannot happily distribute your keys if you do not want to get your DNS messed up.


# What this script does not do?
If you want a self-hosted alternative for no-ip.com or dyndns.com, you should consider to install [nsupdate.info](https://github.com/nsupdate-info/nsupdate.info)

# Installation
The script itself is self-explanatory and nicely commented, I think you'll have no problem at all modifying the variables to your needs.

Put the script wherever you want (for example on /opt/nsupdate/nsupdate-dynip), make sure it's executable.
Then create a cron task to run it. I'm supplying a cron job for you to place on /etc/cron.d/

