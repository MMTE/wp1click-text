# wp1click

wp1click is a WordPress 1 click installer that can be installed as a website hosting control panel

## why?
the idea about wp1click was that web hosting control panels such as Cpanel or Directadmin are too complicated for a simple WordPress website.
so I decided to create a PaaS platform specifically for WordPress. my approach was using Docker containers and Docker swarm orchestrator.
I made the platform as a startup but it didn't go very well. the problem was the resources which are used by containers doesn't worth the price for a simple WordPress website.
on the other side, Cpanel, DirectAdmin, or other hosting solutions usually use a shared Mysql database so the resources which are needed by a WP website reduce to the least.
in my approach I was creating 3 containers:
- WordPress Container 
- Database (Mysql)
- PHPmyadmin (database management UI)
-----
in my solution each of these containers needed resources from Ram and Cpu so it wasn't a budget solution. yes, there are Companies now that use the Container approach to host websites.
for example, Kinsta is a leading company in WordPress hosting. Kinsta uses Linux Containers in their approach but the point is that their prices are starting from at least $30 per month!
so using containers has profits and cons same as everything else.

a huge Cons in my opinion about shared hosting companies is that if the Database goes exposed, all the tenants and clients on the Database are vulnerable.
so you are responsible for keeping safe the Database. on the other side in Containers and orchestrated solutions each tenant has, it's own database. so compromising a container or database wouldn't usually impacts other users.


-----
it's bad idea....
I'm looking deeper and I think multi user shared hosting is kind of outdated aproach maybe
if containers get lighter and lighter then it would be affordable to not use shared hosting? 🤔

----
its all about when a users escapes the privilages of it's own
how bad it is?
----
if user gains access to root system then all shared users data is compromized 


ok it seems linux is not created for jailing users so users can see other folders but they could not have access to files 
