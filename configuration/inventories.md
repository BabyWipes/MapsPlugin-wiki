Setting Inventories
===================

Out of all the sections in this configuration guide, inventories are probably the most complex, but they're actually really simple!

A typical inventory can look like this:

```java
    public void applyInventory(final BattlePlayer p) {
        Inventory i = p.getInventory();

        // Define items. (This is fairly straight forward right?)
        ItemStack HEALTH_POTION = new ItemStack(Material.POTION, 1, (short) 16373);
        ItemStack STEAK = new ItemStack(Material.COOKED_BEEF, 1);
        ItemStack BOW = new ItemStack(Material.BOW, 1);
        ItemStack ARROWS = new ItemStack(Material.ARROW, 64);
        ItemStack IRON_HELMET = new ItemStack(Material.IRON_HELMET, 1);
        ItemStack IRON_CHESTPLATE = new ItemStack(Material.IRON_CHESTPLATE, 1);
        ItemStack IRON_PANTS = new ItemStack(Material.IRON_LEGGINGS, 1);
        ItemStack IRON_BOOTS = new ItemStack(Material.IRON_BOOTS, 1);
        ItemStack IRON_SWORD = new ItemStack(Material.IRON_SWORD, 1);

        p.getInventory().setBoots(IRON_BOOTS); // Set boots
        p.getInventory().setLeggings(IRON_PANTS); // Set pants
        p.getInventory().setChestplate(IRON_CHESTPLATE); // Set chest plate
        p.getInventory().setHelmet(IRON_HELMET); // Set helmet

        // Add items into inventory bar.
        // The numer being the slot number. (Remember: Slot 1 is actually 0, Slot 2 is 1, etc)
        // Second arg is the item being added.
        i.setItem(0, IRON_SWORD);
        i.setItem(1, BOW);
        i.setItem(2, STEAK);
        i.setItem(3, HEALTH_POTION);
        i.setItem(4, ARROWS);
    }
```

---

Now the thing that's confusing with Inventories is actually defining the item, especially since not all items are named as you think they would be. Here's a breakdown of the code to actually define the item:
```java ItemStack IRON_SWORD = new ItemStack(Material.IRON_SWORD, 1); ```

Using the term ```ItemStack``` shows that we're defining an item.
```IRON_SWORD``` is a name we use to reference the item. This does not have to be the actual name of the item, although it usually is.
Using ```new ItemStack``` again shows that we want to create a new ItemStack.
```Material.IRON_SWORD``` is the actual item that we want to use. A full list of items can be found in the [Bukkit API documentation](For a full list of materials, see http://jd.bukkit.org/dev/apidocs/org/bukkit/Material.html).

---

Once we've defined the items we want to add, we need to set them inside the inventory.
The easiest items to set are the armor items. Let's start with these:
```java p.getInventory().setBoots(IRON_BOOTS); ```
It's fairly straightforward. We're getting an inventory and setting the inventory boots to the item name we defined in the previous section.

---

Once we've set the player's armor, we need to give them items that will be used in-game. These can include swords, bows, arrows and other miscellaneous items, such as health potions.
```java i.setItem(0, IRON_SWORD); ```
Here, we're setting the iron sword we defined earlier to the first slot in the player's hotbar.
The '0' in this case signifies the slot where we want to set the item. Note that '0' is the first slot of the player's hotbar, and '8' is the last, even though there are 9 slots in the bar.
Any number above 8 will cause the item to be set in the player's main inventory, and not in the hotbar.

The following image shows the numbers of inventory slots:

![Inventory Slots](http://i.imgur.com/Nof3XLq.png)

Once we've set all the items, we can move on to defining the map region!
Let's set some items...

---

Create a new Iron Sword ItemStack and set it to the third slot of a player's hotbar.

```js
ItemStack IRON_SWORD =
```

```js
ItemStack IRON_SWORD = new ItemStack(Material.IRON_SWORD, 1);
i.setItem(2, IRON_SWORD);
```

```js

```

---