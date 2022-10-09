# smarts dog docs(vrej)

## Table of contents:

 0. [things](#things)
 1. [Tile claiming/doing](#tile-claimingdoing)
 2. [Tile information](#tile-information)
 3. [Tile overriding/modification](#overriding-tiles)
 4. [Tile updating](#tile-updating)

--- 
# things
 - ive added this now instances: you have to be manually assigned one(i don't trust people) and then each instance is seperate
 - the bot prefix is `oooh`
 - the bot raises an InvalidTileError if the tile is invalid
 - you can only override others tiles if you have ManageMessages permission
 - currently all arguments are necessary and are written with `[argument]`, in case there will be unnecessary arguments in the future, they will be written with `{argument}`

---
# Tile claiming/doing
## 1. `claim` command:

**syntax**: `oooh claim [tile]`

- claims a tile(lol)
- If the argument is missing: does nothing and sends error message.
- If the tile is already claimed/done by another player: does nothing and informs the user the status of the tile.
- If successful: updates tile and tells the user they claimed the tile.

## 2. `done` command

**syntax**: `oooh done [tile]`

- Do a tile(lol)
- If the argument is missing: does nothing and sends error message.
- If the tile is already claimed/done by another playr OR the player doing the tile doesn't match with the player that claimed the tile: does nothing and informs the user the status of the tile.
- If the tile is not claimed/does not have data: tells the user to claim the tile first and does nothing.
- If successful: updates tile and tells the user they claimed the tile.

---

# Tile information

## 3. `info` command

**syntax**: `oooh info [tile]`

- gives information of a tile
- If the argument is missing: does nothing and sends error message.
- If the tile does not have data: tells the user the tile does not have data.
- If successful: tells use the mode of the tile, the author, and the timestamp.

## 4. `expire` command

**syntax**: `oooh expire`

- gives 10 closest tiles to expiry in sorted order(if there are less than 10 tiles that have data, output all tiles)

- If successful: outputs tiles and their expiry date(how can you mess this command up it does not have arguments)

---

# Overriding tiles
## 5. `override` command
    
**syntax**: `oooh override [claim/done/timemodify] [tile] {time}`

- either override claim/done/the expiry date of a tile
- If it is `oooh override timemodify`, you need to put in the time argument
- The time argument means the tile until expiry the tile is (1:0 means the tile expires in a a hour, second are not included due to them being insignificant)
- In the backend the function just calls the functions to do the done/claim/timemodify, so they will return their normal output
- You need Manage Messages to override others tiles

## 6. `timemodify` command

**syntax**: `oooh timemodify [tile] [time]`

- Updates the expiry date of a tile
- If missing arguments: tells the user and does nothing      
- If the tile you are trying to modify is not yours: does nothing and informs the user(use override timemodify to override others tiles)

---
# Tile updating

# Auto updating

the bot automatically updates tiles every minute and changes them to neutral if they have expired

## 7. `update` command

**syntax**: `oooh update`
    
- Updates tiles
- Tells user the tiles have been updated

---

# oooh
