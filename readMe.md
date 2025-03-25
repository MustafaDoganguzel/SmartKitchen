# SmartKitchen Project
**Note:** This project is created as a small example to better understand the concept of composition in object-oriented programming.
This project simulates a Smart Kitchen system where different appliances (Coffee Maker, Refrigerator, and Dish Washer) perform specific tasks based on their state.

## Features

- **SmartKitchen**: Manages the state of the kitchen appliances.
- **CoffeeMaker**: Can brew coffee if it has work to do.
- **Refrigerator**: Can order food if it has work to do.
- **DishWasher**: Can wash dishes if it has work to do.
- Appliances are controlled via `setKitchenState()` and perform tasks with `doKitchenWork()`.

## Class Overview

### SmartKitchen

- Manages the three appliances: **CoffeeMaker**, **Refrigerator**, and **DishWasher**.
- Provides methods to set appliance states (`setKitchenState()`) and perform tasks (`doKitchenWork()`).

### CoffeeMaker

- Can brew coffee if `hasWorkToDo` is `true`. Once brewed, it sets `hasWorkToDo` to `false`.

### Refrigerator

- Can order food if `hasWorkToDo` is `true`. After ordering, it sets `hasWorkToDo` to `false`.

### DishWasher

- Can wash dishes if `hasWorkToDo` is `true`. Once done, it sets `hasWorkToDo` to `false`.

## Usage

1. **Set appliance states** using `setKitchenState(coffeFlag, fridgeFlag, dishWasherFlag)`, where each flag corresponds to whether the appliance should perform work.
2. **Call `doKitchenWork()`** to trigger tasks on all appliances.

```java
SmartKitchen kitchen = new SmartKitchen();

// Set appliance states
kitchen.setKitchenState(true, false, true);

// Perform kitchen tasks
kitchen.doKitchenWork();
