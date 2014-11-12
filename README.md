11/11/14 - 11:18:10 P.M.
scott@newgeo.com • @cometbus

#DNS Tools
When you run secondary DNS for others, if they add or delete a DNS zone, the first time these actions happen, changes to the primary have to be made.

They are simple, and amount to adding a domain to a list.

Deleting them is also the same.

The hard part is, when the client does not keep you up to date on what has been added and deleted. In that case, we take a list of all zones on the secondary server, and iterate over them with these scrips.  This will perform a `dig` on the files, looking for if the zone is up to date, or if the domain has expired, and I can delete secondary, etc.