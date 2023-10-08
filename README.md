# Chest System

An advanced chest system featuring various chest types, MVC-S design pattern, Singleton services, and a state machine.

## Features

### Scriptable Objects
- **Chest Types:** Four distinct chest types: COMMON, RARE, EPIC, LEGENDARY.
- **Rewards:** Each chest type gives randomized coins and gems as rewards.
- **Unlocking Time:** Different unlocking times are associated with each chest type.

### Model-View-Controller-Service (MVC-S) Pattern
- **MVC:** The chest system follows the MVC pattern with a Model, View, and Controller for each chest.
- **Service:** A service class is responsible for chest creation.

### Singleton Pattern
- Services like `Chest Service`, `UI Service`, etc. are implemented as Singletons ensuring a single instance.

### State Machine Pattern
- **LOCKED State:**
  - Option to instantly unlock using gems.
  - Begins unlocking timer.
- **UNLOCKING State:**
  - Option to speed up the unlocking process using gems.
  - Displays a countdown until the chest is unlocked.
- **UNLOCKED State:**
  - A prompt to open the chest.
  - A pop-up showcases your rewards upon opening.

### Object Pooling
- Efficient object pooling ensures that only as many chest views are active in the scene as there are chest slots.
