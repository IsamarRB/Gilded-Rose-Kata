# Gilded Rose Inventory System

Welcome to the Gilded Rose Inventory System. This system updates the quality and the `sellIn` (days to sell)
of items on a daily basis according to specific rules.

## Project Description

This project simulates the inventory system of the Gilded Rose Inn. Items in the inventory have
properties `sellIn` and `quality` which are updated daily according to specific rules.

### Updating Rules

- All items have a `sellIn` property which denotes the number of days we have to sell it.
- All items have a `quality` property which denotes how valuable the item is.
- At the end of each day, the system decrements both values for each item using the `updateQuality()` method.
- Once the recommended sale date has passed (`sellIn` < 0), the `quality` degrades at twice the rate.
- The `quality` of an item is never negative.
- Aged Brie cheese' (`Aged Brie`) increases in quality as it gets older.
- The `quality` of an item is never greater than 50, except for `Sulfuras` (`Sulfuras, Hand of Ragnaros`), which has a 
fixed `quality` of 80 and a fixed `quality` of 50.
  a fixed `quality` of 80 and does not change.
- A ‘Backstage passes’ increases in quality as the concert date approaches:
  - If the concert is 10 days or less away, the quality increases by 2 units.

![GildedRose](https://github.com/user-attachments/assets/aa070c7a-336e-46c7-b01a-b55b7788f9a6)

  - If it is 5 days or less, the `quality` increases by 3 units.
  - After the concert, the `quality` drops to 0.
- Conjured’ objects degrade in quality twice as fast as normal objects.

## Project Structure

- **Item.java**: Class representing an item in the inventory.
- **GildedRose.java**: Class containing the logic for updating inventory items.
- **GildedRoseTest.java**: Unit tests to verify the correct functionality of the system.
