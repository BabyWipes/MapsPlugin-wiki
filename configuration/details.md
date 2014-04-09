Basic Map Details
=================

When creating a new configuration, a file for the map should be created.
In this tutorial, we'll be creating a new map called *'Serene Waters'*.
In this case, we would create a new file called ```SereneWaters.java```.

> Let's open up this file in our favorite text editor...

Up the top of our file, we need to state the package our class or file is in.
To do this, we would type: ```package *our package here*;```.
In most OresomeCraft battles maps, the package would be ```com.oresomecraft.maps.battles.maps```. Therefore, our package statement would be: ```package com.oresomecraft.maps.battles.maps;```
Let's also leave a blank line below the package statement.

We then need to import other classes from the Maps Plugin that will help our map work the way we want it to.
We do this by typing ```import *the class we want to import```.
When creating a battles map, we need to import at least three classes.
These classes are the MapConfig class, the BattleMap class and the IBattleMap class.
Let's add these:

```java
import com.oresomecraft.maps.MapConfig;
import com.oresomecraft.maps.battles.BattleMap;
import com.oresomecraft.maps.battles.IBattleMap;
```

Let's also add all of the bukkit and OresomeBattles classes:

```java
import org.bukkit.*;
import com.oresomecraft.OresomeBattles.api.*;
```

After that, let's leave a blank line and add our class statement. When creating a battles map, the class statement would be somewhat like this:

```java
@MapConfig
public class SereneWaters extends BattleMap implements IBattleMap, Listener {
}
```

where 'SereneWaters' is the name of our map file, without the .java extension.

We now need to add a constructor. The constructor is where all the attributes of the map will be stored. For now, we don't need to add any attributes; so our constructor will look like this:

```java
    public SereneWaters() {
        super.initiate(this, name, fullName, creators, modes);
    }
```

Finally, we need to add the actual details of our map! We need to add: The name of the world in which our map is stored, the full name of the map, who created the map and the gamemodes we want the map to be played with.

```java
    // Map Details
    String name = "serenewaters";
    String fullName = "Serene Waters";
    String creators = "psgs and SuperDuckFace";
    Gamemode[] modes = {Gamemode.TDM, Gamemode.FFA};
```

Our map class should now look like this:

```java
    package com.oresomecraft.maps.battles.maps;

    import com.oresomecraft.maps.MapConfig;
    import com.oresomecraft.maps.battles.BattleMap;
    import com.oresomecraft.maps.battles.IBattleMap;
    import org.bukkit.*;
    import com.oresomecraft.OresomeBattles.api.*;

    @MapConfig
    public class SereneWaters extends BattleMap implements IBattleMap, Listener {

        public SereneWaters() {
            super.initiate(this, name, fullName, creators, modes);
        }

        String name = "serenewaters";
        String fullName = "Serene Waters";
        String creators = "psgs and SuperDuckFace";
        Gamemode[] modes = {Gamemode.TDM, Gamemode.FFA};
    }
}
```

Awesome! We've now configured the basic details of a battles map.
Now it's time for you to try it yourself...

---

Create the basic details for a map called Tropical Wasteland, by Afridge1O1 that would be played with the FFA gamemode.
To get you started, we've already added the package and import statements.

```js
package com.oresomecraft.maps.battles.maps;

import com.oresomecraft.maps.MapConfig;
import com.oresomecraft.maps.battles.BattleMap;
import com.oresomecraft.maps.battles.IBattleMap;
import org.bukkit.*;
import com.oresomecraft.OresomeBattles.api.*;

```

```js
    package com.oresomecraft.maps.battles.maps;

    import com.oresomecraft.maps.MapConfig;
    import com.oresomecraft.maps.battles.BattleMap;
    import com.oresomecraft.maps.battles.IBattleMap;
    import org.bukkit.*;
    import com.oresomecraft.OresomeBattles.api.*;

    @MapConfig
    public class TropicalWasteland extends BattleMap implements IBattleMap, Listener {

        public TropicalWasteland() {
            super.initiate(this, name, fullName, creators, modes);
        }

        String name = "tropicalwasteland";
        String fullName = "Tropical Wasteland";
        String creators = "Afridge1O1";
        Gamemode[] modes = {Gamemode.FFA};
     }
}
```

```js

```

---