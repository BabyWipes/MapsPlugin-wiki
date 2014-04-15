Spawn Points
============

Once you've added the [basic map details](), it's time to add some spawn points for players to spawn at.
Each battles map requires at least two types of spawns, TDM spawns and FFA spawns.
The reason behind this is that even if the map only uses the TDM gamemode, spectators will use FFA spawns to be spawned in the game.

To start off, let's add a container for our TDM spawns. In Java, certain code must be placed in [methods](http://www.tutorialspoint.com/java/java_methods.htm) so that it can be executed by the MapsPlugin.
We're going to name our method 'readyTDMSpawns'. It's going to be a public method, meaning that the Maps Plugin can access it, and it won't return anything, so it will be void.

```java
public void readyTDMSpawns() {

}
```

Inside that method, let's add our spawns...

```java
public void readyTDMSpawns() {
redSpawns.add(new Location(w, 18, 28, 84, -154, 0));
redSpawns.add(new Location(w, 13, 25, 61, 180, 0));
blueSpawns.add(new Location(w, -110, 21, 43, 18, 0));
blueSpawns.add(new Location(w, -83, 21, 13, 176, 0));
}
```

Let's break down the co-ordinates shown.
For example, let's use the co-ordinates of the first spawn:
```(new Location(w, 18, 28, 84, -154, 0));```
The first three co-ordinates represent the x, y and z axes, in that order.
These can be found in-game, by pressing the F3 key:

![In-game Cords](http://i.imgur.com/qGJYm0B.png)

The last two co-ordinates are slightly different.
The second last co-ordinate represents yaw, which is the direction which the player is facing.
Adding yaw to spawn co-ordinates is essential when configuring a map in order to stop players spawning backwards and getting confused.

![In-game Yaw](http://i.imgur.com/8Fs8cX7.png)

The last co-ordinate represents pitch, which is the the angle a player's head is facing while in-game.
Pitch is used very rarely, so it won't be covered in this chapter.

---

Once we've added the TDM spawns, we can add the FFA spawns!
Adding FFA spawns is nearly the same as adding TDM spawns, except the [method name](http://docs.oracle.com/javase/tutorial/java/javaOO/methods.html) will be different.
In this case, let's name our method 'readyFFASpawns'.

```java
public void readyFFASpawns() {
        FFASpawns.add(new Location(w, 18, 28, 84));
        FFASpawns.add(new Location(w, 13, 25, 61));
        FFASpawns.add(new Location(w, -10, 25, 38));
        FFASpawns.add(new Location(w, -53, 23, 19));
}
```

All done!
Now let's give it a try...

---

Create a blue and red TDM spawn.
The blue spawn should have the following co-ordinates: ```18, 62, 32, -90, 0```
The red spawn should have the following co-ordinates: ```14, 98, 22, 183, 0```

```js
redSpawns.add(
```

```js
redSpawns.add(new Location(w, 18, 62, 32, -90, 0));
blueSpawns.add(new Location(w, 14, 98, 22, 183 0));
```

```js

```

---