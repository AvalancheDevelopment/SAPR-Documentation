# SAPR Tower Disabling

> **_NOTE:_** Radio tower simulation must be enabled for this feature to work.

The SAPR in-game script allows for the radio towers to be disabled for 15 minutes, preventing communications on the radio trunk. The script supplies its own minigame that can be used for this feature, but also allows for developers to integrate their [own way of doing it](#Custom_Implementaton).

## Disabling This Feature

This feature can be disabled if you do not want to use it. To disable this feature, set the `sapr_useOwnMinigame` convar to true. Example of what the SAPR.cfg would look like:

```
setr sapr_useOwnMinigame true
```

### Provided Implementation

The provided implementation has two locations in county (commonly referred to as 'Blaine County') and two locations in the city (commonly referred to as 'Los Santos') which can be used for this feature. Players will see a prompt when at one of these locations to press a button to begin the minigame.

Once the minigame begins, the player will have 5 seconds to memorize a layout of colored squares in a 5x5 grid. Then, they will have 10 seconds solve the puzzle by click all the squares that were colored. If they succeed, all radio towers, including mobile repeaters, will be disabled for 15 minutes. During that time, only direct radio channels will work (talkaround channels that don't use the radio trunk).

After the 15 minutes is up, radios will begin the process of reacquiring radio signal from any available towers or repeaters.

### Custom Implementation

To begin using a custom implementation, first set the `sapr_useOwnMinigame` convar to true. Example of what the SAPR.cfg would look like:

```
setr sapr_useOwnMinigame true
```

The rest of the implementation is up to you. You can define as many locations as you like, what (if any) minigame would required to be succeed in disabling the towers, and any other parameters, cooldowns, etc. you would like.
**The only requirement is that when a player succeeds, a server event needs to be triggered for `SAPR:DisableRadioTowers`**.

```lua
TriggerServerEvent("SAPR:DisableRadioTowers");
```
