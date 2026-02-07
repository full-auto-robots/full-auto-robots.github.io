# Making An FRC Dashboard

Okay so for whatever reason, DriveTools isn't good enough for you. Instead of emailing me at `full-auto-robots@gmail.com` and explaning what you would add (do consider reaching out, I want this software to be as good as possible) you just want to make your own software. 

Fine. That's pretty much what I did when I made DriveTools in the first place. Read on, then.

## A word of warning

Programming an FRC Dashboard from scratch is not easy. Unlike programming an FRC robot, nobody is giving you template projects that you can build off of and there are less people who are going to have the same problems as you. If you are an inexperienced software developer, I'd be weary of trying something like this out.

It's not that I don't think it'll work as a learning experience. I actually think the opposite, diving into a project tends to teach you a lot (check out the [old DriveTools](https://github.com/full-auto-robots/drivetools-OLD) to see the difference between my skills then and now). 

But notice how I said *software developer*, not *coder*? If you want to make a dashboard and plan on publishing it, you've gotta make some smart decisions when designing it. Otherwise you'll hit roadblocks later.

I'm not here to give a course on software design (I don't think I'm really qualified to, anyhow). If you're thinking about it, why not try it? Just don't be afraid to start things over if necessary.

## Building off of DriveTools

The source files are on GitHub, after all. I might write a tutorial on how to modify DriveTools later, but really all you need to do to start messing around is download [Unity](https://unity.com/) - which is free. That's the engine that I used to make DriveTools.

I actually recommend *not* doing this. The above warning not only still applies, but I think you'll be worse off. Things might get complicated if you're trying to do more than tweak a few things.

You're welcome to try it, though. 

*(Just don't go acting like you made it yourself.)*

## Vital resources

The most important thing when making an FRC Dashboard is the ability to work with NetworkTables. I wrote DriveTools in `C#`, the language that Unity uses, so I needed a version of NetworkTables that worked in C#. Finding this was actually the reason that I set out to make DriveTools in the first place.

You have three options:

* NT3, as a wrapper:

* NT3, fully translated:

* NT4: