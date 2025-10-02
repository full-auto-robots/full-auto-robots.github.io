## Image Display Nodes

These allow you to define some images, and the display will pick one of them based on the value that it sees on NetworkTables.
It works like an array. A value of 0 on NetworkTables will load the first image, a value of 1 the second, and so on.
You also define a default image to use when the value doesn't have an image associated with it.

This can be used for a few different things, but mostly making your dashboard look better:
* showing what 'mode' your robot is in
* displaying what elevator level is selected with a picture of the elevator
* creating boolean indicators with images that are either red or green
* putting information on the dashboard via static images
