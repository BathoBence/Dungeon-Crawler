
# Dungeon Crawl

## Purpose

[Roguelikes](https://en.wikipedia.org/wiki/Roguelike) are one of the oldest
types of video games. The earliest ones were made in the 70s, and they were inspired
a lot by tabletop RPGs. Roguelikes usually have the following features in common.

- They are tile-based.
- The game is divided into turns, that is, you take one action, then the other
  entities (monsters, allies, and so on, controlled by the CPU) take one.
- The task is usually to explore a labyrinth and retrieve some treasure from its
  bottom.
- They feature permadeath: if you die, it's game over, you need to start from the
  beginning again.
- They rely heavily on procedural generation: Levels, monster placement, items, and so on
  are randomized, so the game does not get boring.

My task was to create a roguelike. Through this project, I've got a better grasp on OOP.

## What have I learned?

- Got more practice in OOP.
- Understand design patterns: layer separation. (All of the game logic, such as player
  movement, game rules, and so on), is in the `logic` package, completely
  independent of user interface code.

## Tasks

1. Analyze the project\
   Understand the existing code, classes, and tests so you can make changes.

2. Restrict movement\
   Create a game logic which restricts the movement of the player so they cannot run into walls and monsters.
    - The hero is not able to move into walls.
    - The hero is not able to move into monsters.

3. Dungeon items\
There are items lying around the dungeon. They are visible in the GUI. 
   - There are at least two item types, such as a key and a sword(Armor, weapon, potion).
   - There can be one item in a map square.
   - A player can stand on the same square as an item.
   - The item must be displayed on screen (unless somebody stands on the same square).

4. Pick up items\
Create a feature that allows the hero to pick up an item.
   - There is a way to pick up items (Space key).
   - After the player picks up the item, the item the hero is standing on is gone from map.

5. Show picked up items\
   Show picked up items in the inventory list.
   - There is an `Inventory` list on the screen.
   - After the hero picks up an item, it appears in the inventory.

6. Attack monsters\
   Make the hero able to attack monsters by moving into them.
   - Attacking a monster removes 5 health points. If the health of a monster goes below 0, it dies and disappears (Leaves corpse).
   - If the hero attacks a monster and it does not die, it also attacks the hero at the same time (it only removes 2 health points).
   - Having a weapon increases attack strength.
   - Different monsters have different health and attack strengths (basic skeleton, Kraken boss).


7. Different monsters\
   Create three different monster types with different behaviors.
    - There are at least two different monster types with different behaviors.
    - One type of monster does not move at all.
    - One type of monster moves randomly. It cannot go trough walls or open doors.

9. More map features\
    Create maps that have more varied scenery. (Shop)
    - At least three more tiles are used. These can be more monsters, items, or background. At least one of them must be not purely decorative, but have some effect on gameplay.



## Hints

- Open the project in IntelliJ IDEA. This is a Maven project, so you need to
  open `pom.xml`. The project uses JavaFX, so use the `javafx` Maven plugin to
  build and run the program. Build using `mvn javafx:compile`, and run using `mvn javafx:run`.

## Screenshots

![Alt text](./Screenshots/Képernyőkép%202024-06-06%20102816-1.png?raw=true "Optional Title")

![Alt text](./Screenshots/Képernyőkép%202024-06-06%20102847.png?raw=true "Optional Title")

![Alt text](./Screenshots/Képernyőkép%202024-06-06%20102925.png?raw=true "Optional Title")
