# nsupdate-dynip

You can use this small script to update a BIND server from a outside client machine, to use BIND as a Dynamic DNS server.

You must note that in order to make this work, the client side will need a valid key generated from the server and properly configured on the server-side named.conf. You can [duck for it](https://duckduckgo.com/?q=painless+dynamic+dns), there are plenty howtos on the Net.

Also note that anyone who have that certificate can modify you DNS zone, so you cannot happily distribute your keys if you do not want to get your DNS messed up.

If you want a self-hosted alternative for no-ip.com or dyndns.com, you should consider to install [nsupdate.info](https://github.com/nsupdate-info/nsupdate.info)

The script itself is self-explanatory and nicely commented, I think you'll have no problem at all modifying the variables to your needs.

