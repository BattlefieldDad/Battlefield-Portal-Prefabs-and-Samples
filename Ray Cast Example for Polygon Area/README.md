Working on a version of secure area for Battlefield Portal I came across the problem of checking whether players are in a given area.
This is complicated by the fact that areas may not be square and may not be exactly aligned with the X and Z axis.
Still working on this but made sense to use a ray casting technique to check if the player is in the given area.
There are a variety of different examples of code but restrictions on the number of variables available to use in portal
plus difficulties with getting the right syntax using blocks (much easier when dealing with these things through text based languages)
I needed a concise way of running the checks on the player position while still keeping code manageable withing portal and allowing me to use the least number of variables possible AND allowing me to build it in a flexible way so that others could just hook into it.

Some information on the principles of ray casting are avialable here: https://www.geeksforgeeks.org/how-to-check-if-a-given-point-lies-inside-a-polygon/
This gives a good overview of the principle behind it, however the code provided is difficult to translate over into the portal rules editor.

Enter this algorithm by w.Randolph Franklin
https://wrf.ecse.rpi.edu/Research/Short_Notes/pnpoly.html

Although there are some minor issues with this algorithm, given its simplicity, it seemed perfectly suited to this use case.

I have used this algorithm (with some modifications to allow for the portal rules editor as well as to allow position to be matched against the player and also allow other portal creators an easier method of setting their own areas)

It is still quite complex for the rules editor and I have yet to test it under load but currently this is working really well.
