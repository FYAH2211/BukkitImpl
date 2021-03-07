# Lunar Client Bukkit API Implementation
> Quick and Easy Setup to LunarClient integration 

## Introduction

This is a simple bukkit plugin which will allow you and your server to quickly integrate lunar features.
This is most likely intended for small teams or servers who just need a couple basic features and the ability to disable 
mods.

This project can be added as a plugin, built on, or taken inspiration from for creating server sided LunarClient features.

### What this is NOT

This is not ideal for huge servers who need peak performance 24/7 and want to do a wide variety of gameplay features based off
timings or other gameplay events. While this plugin is efficient, this is a one size fits most which is usually not ideal for 
performance critical servers or applications. If you want a more technical, full control API to implement [BukkitAPI](https://github.com/LunarClient/BukkitAPI) is probably
the best bet.

## How to Install

* Download the built jar from [here](TODO).
* Fully stop the bukkit server
* Add the jar to the `plugins` folder.
* Start the server and enjoy!

## How to edit the Configuration (config.yml)

* Once the plugin is installed, a folder named `LunarClient-Impl` should be created in your plugins folder.
* Shut down the bukkit server.
* Open the config.yml in a word editor

### How to disable mods

By default `skyblockAddons` comes disabled, ideally you would remove this as this is just an example of how to disable a mod.

* Find the mod ID for the mod you wish to disable 
  * Most can be found in the config.yml.
* Add the modId to the list under the header named `force-disabled-mods:`

#### Example:
Example of how to disable freelook

```yaml
# freelook - Freelook
force-disabled-mods:
  - "freelook" 
```

### How to add a waypoint

By default there is a waypoint at 0, 0 called "Spawn" for world "world"

#### Overworld Spawn Example:
```yaml
  - Spawn: # The same name as the waypoint.
      x: 0 # Must be a number, -inf->inf. No decimals. No quotes.
      y: 100 # Must be a number, 0->255. No decimals. No quotes.
      z: 0 # Must be a number, -inf->inf. No decimals. No quotes.
      name: "Spawn" # MUST be a word, and MUST be in quotes.
      world: "world" # MUST be a word, and MUST be in quotes. MUST be a valid world name.
      color: 0xFF0000 # MUST be a hexadecimal representation of a number.
      forced: false # MUST be either a true or false value. No quotes.
      visible: true # MUST be either a true or false value. No quotes.


```

#### End Portal Example:

_Note: This is not an actual location, this is an example._
```yaml
  - Portal: # The same name as the waypoint.
      x: 103 # Must be a number, -inf->inf. No decimals. No quotes.
      y: 65 # Must be a number, 0->255. No decimals. No quotes.
      z: 202 # Must be a number, -inf->inf. No decimals. No quotes.
      name: "Portal" # MUST be a word, and MUST be in quotes.
      world: "world_the_End" # MUST be a word, and MUST be in quotes. MUST be a valid world name.
      color: 0xFFAA00 # MUST be a hexadecimal representation of a number.
      forced: true # MUST be either a true or false value. No quotes.
      visible: true # MUST be either a true or false value. No quotes.
```