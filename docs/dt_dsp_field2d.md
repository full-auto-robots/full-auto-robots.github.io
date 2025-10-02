# Field2D Displays

[image of what it looks like]

These are one of the most useful display objects that you can use. They can be used to visualize data coming from the bot, or upload data to the robot, or even command the robot by sending it coordinates. You could use them to see the position/rotation of the robot, show paths and shapes, things like that.

## Things to be familiar with:

* [robot programming](https://full-auto-robots.github.io/#dt_rob_about/) with DriveTools

* the [nav_robot](https://full-auto-robots.github.io/#dt_rob_nav_robot/) class
* the [nav_path](https://full-auto-robots.github.io/#dt_rob_nav_path/) class
* the [nav_field](https://full-auto-robots.github.io/#dt_rob_nav_field/) class

## Getting The Data

Field2D displays can take in one of TWO data types from NetworkTables. Either a nav_robot by itself, or a whole nav_field class if you want to display more than a robot's position and rotation. In any case, just [edit the display](https://full-auto-robots.github.io/#dt_dsp_editing/) and set the NT Key to wherever your data class is located.

***

## Elements of A Field

### Robots

If you read the page about the `nav_robot` class, then you'll know what kind of data you'll need. Field2D nodes have an array of nav_robot classes, which get turned into strings the same way that an individual nav_robot class would via nav_robot.EncodeToString().
This is done so that tracking multiple bots can be supported. 

### Paths

Field2D nodes have an array of nav_path classes as well. These can represent really whatever you want, as long as whatever you want is a collection of points in 3D space. Some ideas:
* A trail showing where the robot has been
* A visualization of an auto
* Estimated positions of the robot (though you could use more nav_robot classes for this)

### Markers

Field markers (the `nav_marker` class) represent things. They're just images that have a position, rotation, and scale. You can use them to represent Apriltags that the robot can see, game pieces that it has detected, or you can use them as ways to show events like an impact (which could ruin odometry). You can draw anything you want using `nav_path` classes, but using a `nav_marker` is usually quicker.

***

## The Field Editor

As mentioned at the top of this page, Field2D nodes can also be used to _send_ data as well as receive it. You do this by clicking the little pencil icon in the top left of the display, which opens the _field editor_.

[image of editor button]

This editor allows you to manually draw paths, place robots, or place markers on the field by clicking.

### Adding/Removing Field Elements

Field elements of each type can be added by clicking the plus icon next to the name. You'll see an entry appear in the corresponding list for the new field element, and depending on what it is you can place it onto the field.

* For paths, creating a new path puts the editor into 'draw mode'. You click to place new path points, and either press 'Enter' or click the checkmark button to finish drawing the path.
* For robots/markers, just move your mouse to wherever you want to place it and left-click to place. Before you place it, you can use the scrollwheel to rotate it.

After placing a field element you can change it via the list entry. Paths can be re-drawn and their color can be changed, robot settings can be edited, and so on.

Removing a field element is as simple as clicking the red 'x' to the right of it's entry in the list.

### Uploading The Finished Field

When finished, you can click the 'save' button. This will convert the field that you made into a string, and send it to NetworkTables. Now any code that you set up to read from that NetworkTables key can use the field data for whatever you want. 

Also, pressing the save button will tell Drivetools to save the data in the loaded layout (.lyt file) automatically. That way, closing and re-opening the software will preserve exactly the field in the editor. Not all NetworkTables data gets saved in the layout! It's only the data that _you yourself pushed manually_.

### Trying To Get/Receive Data At The Same Time

...just don't. Don't try this. When in the field editor the Field2D node will _in theory_ ignore whatever's happening on NetworkTables, but it's better to not try and use the Field2D nodes as two-way, unless you _really_ know what you're doing.
