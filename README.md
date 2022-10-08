# smarts dog docs(vrej)

## Table of contents:
### 0. things
### 1. Tile claiming/doing
### 2. Tile information
### 3. Tile overriding/modification
### 4. Tile updating

--- 
# things
 - ive added this now instances: you have to be manually assigned one(i don't trust people) and then each instance is seperate
 - the bot prefix is ```oooh```
 - the bot raises an InvalidTileError if the tile is invalid
 - you can only override others tiles if you have ManageMessages permission
 - currently all arguments are necessary and are written with ```[argument]```, in case there will be unnecessary arguments in the future, they will be written with ```{argument}```

---
# tile claiming/doing
### 1. claim command:
    1a. syntax:
        ```oooh claim [tile]```
    1b. details
        claims a tile(lol)
    1c. output
        If the argument is missing: does nothing and sends error message
        If the tile is already claimed/done by another player: does nothing and informs the user the status of the tile
        If successful: updates tile and tells the user they claimed the tile
### 2. done command
    2a. syntax:
        ```oooh done [tile]```
    2b. details
        do a tile(lol)
    2c. output
        If the argument is missing: does nothing and sends error message
        If the tile is already claimed/done by another playr OR the player doing the tile doesn't match with the player that claimed the tile: does nothing and informs the user the status of the tile
        If the tile is not claimed/does not have data: tells the user to claim the tile first and does nothing
        If successful: updates tile and tells the user they claimed the tile
---
# tile information
### 3. info command
    3a. syntax
        ```oooh info [tile]```
    3b. details
        gives information of a tile
    3c. output
        If the argument is missing: does nothing and sends error message
        If the tile does not have data: tells the user the tile does not have data
        If successful: tells use the mode of the tile, the author, and the timestamp
### 4. expire command
    4a. syntax
        ```oooh expire```
    4b. details
        gives 10 closest tiles to expiry in sorted order(if there are less than 10 tiles that have data, output all tiles)
    4c. output
        If successful: outputs tiles and their expiry date(how can you mess this command up it does not have arguments)
---
# overriding tiles
### 5. override command
    5a. syntax
        ```oooh override [claim/done/timemodify] [tile] {time}```
    5b. details
        either override claim/done/the expiry date of a tile
        if it is ```oooh override timemodify```, you need to put in the time argument
        the time argument means the tile until expiry the tile is (1:0 means the tile expires in a a hour, second are not included due to them being insignificant)
    5c. output
        in the backend the function just calls the functions to do the done/claim/timemodify, so they will return their normal outputs
        you need ManageMessages to override others tiles
### 6. timemodify command
    6a. syntax
        ```oooh timemodify [tile] [time]```
    6b. details
        updates the expiry date of a tile
    6c. output
        If missing arguments: tells the user and does nothing
        If the tile you are trying to modify is not yours: does nothing and informs the user(use override timemodify to override others tiles)
---
# tile updating
### auto updating
    the bot automatically updates tiles every minute and changes them to neutral if they have expired
### 7. update command
    7a. syntax
        ```oooh update```
    7b. details
        updates tiles
    7c. output
        tells user the tiles have been updated
---












# oooh
