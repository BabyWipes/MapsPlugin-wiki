Map Attributes
==============

In the first section of this wiki, when we were learning about map details, you may remember seeing the word "map attributes" in the constructor section.
Attributes can be added to any map in the map constructor.
Remember this map constructor?

```java
    public SereneWaters() {
        super.initiate(this, name, fullName, creators, modes);
    }
```

Attributes usually affect the map as a whole and can set thing such as the in-game time of day that the map is played at, or whether building on the map is allowed.
An attribute that stops people from building on a map can look like this:
```setAllowBuild(false);```
A full list of attributes can be found in the [Attributes Gist](https://gist.github.com/psgs/10569729)

Once added, an attribute can look like this:

```java
    public SereneWaters() {
        super.initiate(this, name, fullName, creators, modes);
        setTDMTime(8);
        disableFireSpread(true);
    }
```