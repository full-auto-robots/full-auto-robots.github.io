# The \_ROBOT\_ Folder

After downloading Drivetools and unzipping the .zip file, you should see one folder in particular called "\_ROBOT\_".
This folder has nothing to do with Drivetools itself, and instead contains java code for use in your robot project. 
You may delete the folder entirely, move it, or just completely ignore it. It's just example code.

The main reason for the folder's existence is that Drivetools transforms its complicated data classes into strings before sending them over NetworkTables, 
and writing code to turn these strings back into useful data. So I'm providing all of the code to do that for you.

***

The folder contains scripts for the following:

* [field data](https://full-auto-robots.github.io/#dt_rob_nav_field/)
* [path data](https://full-auto-robots.github.io/#dt_rob_nav_path/)
* [robot data](https://full-auto-robots.github.io/#dt_rob_nav_robot/)

_(all of these classes start with the prefix 'nav_' _which stands for 'navigation'. 
That's the naming convention that I use internally within Drivetools, but feel free to change it)_

***

It's worth noting that as you update Drivetools, the code you have on your robot may possibly stop working. 
It's unlikely, but if bugs do occur then update the .java files to the ones found in the \_Robot\_ folder from the version you're actually using.
