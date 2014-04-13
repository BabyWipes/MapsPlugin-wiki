Map Abilities
=============

Many abilities can be added to enhance any OresomeBattles map.
For example, items can be named before that are added to an inventory...
```java InvUtils.nameItem(IRON_SWORD, ChatColor.RED + "Blade of death!");```
It is important to remember that when adding abilities to inventory items, the code that creates the ability must be added before the item is set in an inventory (```i.setItem(0, IRON_SWORD)```).

Other abilities can be added by handling events that occur in game, for example removing arrows from the ground after they have been shot:

```java
    @EventHandler
    public void arrowAway(org.bukkit.event.entity.ProjectileHitEvent event) {
        org.bukkit.entity.Entity projectile = event.getEntity();
        Location loc = projectile.getLocation();
        if (loc.getWorld().getName().equals(name)) {
            if (projectile instanceof org.bukkit.entity.Arrow) {
                org.bukkit.entity.Arrow a = (org.bukkit.entity.Arrow) projectile;
                a.remove();
            }
        }
    }
```

Abilities that handle events are always placed at the bottom of a map configuration file, just before the last ```}``` character.

A list of easy-to-add abilities can be found at the [MapsPlugin repository](https://github.com/OresomeCraft/MapsPlugin/wiki/Advanced-Map-Options) as well as a list of [not-so-easy-to-add-abilities](https://github.com/OresomeCraft/MapsPlugin/wiki/Special-Abilities).