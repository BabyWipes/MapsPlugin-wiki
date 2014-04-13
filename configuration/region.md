Map Region
==========

Each Oresome Battles map has a certain region.
This region is defined by a set of co-ordinates, marking the top left and bottom right bounds of the map.
It is essential that each map has a set of region co-ordinates, as they are often used to make sure players are playing inside the map.

Here's a typical set of co-ordinates defining a map's region...
Remember that anything after two backslashes (//) is a comment and is ignored by the Maps Plugin.

```java
    // Region. (Top corner block and bottom corner block.
    // Top left corner.
    public int x1 = -207; // X location
    public int y1 = 52; // Y location
    public int z1 = -1220; // Z location

    // Bottom right corner.
    public int x2 = -38;  // X location
    public int y2 = 112; // Y location
    public int z2 = -1125; // Z location
```

Let's take a look at the first co-ordinate...
```public int x1 = -207;```

We're defining an [integer](http://en.wikipedia.org/wiki/Integer) variable that can be accessed by the Maps Plugin.
"int" stands for integer and "public" means that the co-ordinate can be accessed by other files (classes).
The number in this case, is the X co-ordinate of the top left corner of the map.

Defining a map's region is fairly straightforward. Simply travel to the top left and bottom right corners of the map, then enter the x, y and z co-ordinates of those locations...