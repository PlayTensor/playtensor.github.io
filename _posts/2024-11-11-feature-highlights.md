---
layout: post
title:  "Feature Highlights"
date:   2024-11-11 12:00:00 -0700
categories: devlog
---

One of the central defining goals of *Tensor 1* is to combine the technical simplicty and elegance of the Greatest Generation/Silent Generation shooter with the narrative focus and world-building of the Generation X shooter [genres]({% post_url 2024-10-24-the-genre-of-tensor %}). In order to achieve this, *Tensor 1* focused on a four main pillars in its technology and design.

### Tile-Based World

The jump from the Greatest and Silent Generation era shooter to the Boomer shooter was marked by the release of Doom in 1993 which, among many other technical innovations, featured non-orthogonal walls, ceilings and floors of variable heights, twists and turns.  No longer would shooters be constrained to the square tile grids of the Greatest Generation and Silent Generation era shooters like Wolfenstein 3D (1992).

But something was sacrificed in that transition, and that was the speed of content creation and iteration made possible by the simplicity of the square tile. Building worlds out of tiles is incredibly simple and fast, making creation and iteration fast. It is said that by the end of development, level designers working on Wolfenstein 3D could create an entire level in a single day.

*Tensor 1* seeks to recapture this simplicity, which allows it to come with a built-in tile based level editor that anyone can use. Simply load up the editor, place a few tiles, hit play, and within seconds you can explore a world of your own creation.

For additional resources on using the tile-based level editor, see the official [game manual]({% link manual/editor/index.md %}) or reach out to [contact.magentagrid@gmail.com](mailto:contact.magentagrid@gmail.com) with questions, documentation requests, and feature requests.

### Physics

However, the danger of building a world out of tiles is that it can feel sterile and static, a big problem for something trying to feel as dynamic and interactive as the worlds of the classic Gen-X shooters of the late 1990s and early 2000s. To that end, *Tensor 1* makes use of physics objects and interactions. *Tensor 1* uses the Bullet physics library for basic rigidbody calculations, along with custom written physics for the behavior of certain key physics objects, particularly the behavior of the force claw, one of the key tools in the player's arsenal. Progression through the world of *Tensor 1* requires mastery of the force claw and its ability to pull and push physics objects, whether to remove physical door locks, place a battery into an empty power slot, or throwing an explosive drone back at the enemy soldier that threw it.

### Artificial Intelligence

Of course, a dynamic world means more than just physics objects. The world also needs to be populated by dynamic monsters, powered by a flexible artificial intelligence (AI) system. *Tensor 1* makes use of two main types of AI, one for its hovering drones, and one for its infantry soldiers.

The AI of the hovering drones is primarily based on steering behavior. The drones regularly scan their surrounding area and applies a modifying force to its current velocity in order to chase its target while avoiding obstacles.

The soldier AI is more complex, intentionally modeled after the celebrated AI systems used in defining Gen-X shooters such as Half-Life (1998). To that end, the soldier AI makes use of finite state machines (FSM), goals, tasks, and schedules. Added all together, the result is an AI that can find and take cover in response to player position, decide when to attack and when to retreat, flush the player out of their cover by deploying allied drones, and, if the player isn't careful enough, outflank and surprise the player.

### Multiplayer

AI opponents, no matter how advanced, still cannot capture that certain special thrill of competing against another living, breathing, thinking person. For that reason *Tensor 1* comes with a competitive Local Area Network (LAN) multiplayer mode, a feature that was once universal during the era of Boomer and Gen-X shooters. In addition to Deathmatch and Team Deathmatch, *Tensor 1* multiplayer includes a Capture the Flag mode where the flags are physics objects that players can grab and manipulate with the force claw.