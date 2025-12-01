# What's DriveTools?

DriveTools is a customizable FRC Dashboard (a program that allows you to display data coming in from an FRC robot). It's meant for use both in-house for testing and in-competition during matches.

Basically, it tries to combine the best of data visualization programs like AdvantageScope and dashboards like Elastic. The goal is to create a software that can do both, very effectively. A one-stop-shop for robot programming and driving.

It communicates with FRC robots using `NetworkTables` (specifically the `NT3` protocol). What is that? Find out [here](https://full-auto-robots.github.io/#dt_net_basics/) or [here](https://docs.wpilib.org/en/stable/docs/software/networktables/networktables-intro.html), more specifics [here](https://docs.wpilib.org/en/stable/docs/software/networktables/index.html). *Code examples are usually provided when talking about robot code, but it's always good to have background knowledge.*

## Why did you make it?

I don't have a nice, clean answer to this question. I guess after realizing that a custom dashboard was within reach, I just wanted to try making one. So there, *curiosity* is the best answer I can give. All the rest I found out *after* I had already started.

Still, now that DriveTools exists I can do a lot more interesting things with FRC robots. It makes it easy to display stuff *other* than a single robot on the field display, which for one is very useful. That said I may have just not looked at other softwares that can do this.


## Why did you make a dashboard with a game engine?

Right so the observant among you have realized that DriveTools was made with the Unity game engine. I did this for two reasons: 

* One, I was already familiar with both it and C#, and the NetworkTables plugin I found worked with it.

* Two, I knew I wanted 3D functionality in DriveTools, and Unity had built-in 3D rendering. I hadn't written any 3D renderers by that time, and thought that was way further out of reach.