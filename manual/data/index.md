---
layout: page
title: Data
parent: Manual
permalink: /manual/data
nav_order: 5
---

{: .warning }
Modifying your save data can potentially break your game. We do not provide a warranty for damage done to the game through data modification.

### Introduction
Player save data is usually kept hidden from the player for a number of reasons, most notably the possibility of players accidentally breaking their copy of the game. However, we believe that paying customers have the right to attempt to modify their own data so long as they understand the implications of doing so.

### Windows PC (Steam)

{: .warning }
Steam Cloud will automatically attempt to save and sync your save data. If you modify your data, you can potentially upload corrupt data that will break your data across all computers that uses your Steam Cloud data.

All relevant user save data is stored in the following file directory: ```%APPDATA%\Godot\app_userdata\Tensor\```
Files with the ```.res``` are a binary file format. It is highly discouraged to attempt to modify these. Most other files are in plain text and should be human readable. However, it is recommended not to modify these files without a solid understanding of potential implications. There is no warranty for games broken by modifying user data files.

### Versions before 1.1
Old versions of the game before 1.1.0.0 unfortunately use a different directory reference: ```%APPDATA%\Godot\app_userdata\Tensor 1\```
If the above directory appears, it is highly recommended to copy files over to the new directory reference: ```%APPDATA%\Godot\app_userdata\Tensor\```