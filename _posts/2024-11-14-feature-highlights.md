---
layout: post
title:  "Feature Highlights"
date:   2024-11-14 12:00:00 -0700
categories: devlog
---

One of the central defining goals of *Tensor 1* is to combine the technical simplicty and elegance of the Greatest Generation/Silent Generation shooter with the narrative focus and world-building of the Generation X shooter [genres]({% post_url 2024-10-24-the-genre-of-tensor %}). In order to achieve this, *Tensor 1* focused on a three main pillars in its technology and design.

### Tile-Based World

The jump from the Greatest and Silent Generation era shooter to the Boomer shooter was marked by the release of Doom in 1993 which, among many other technical innovations, featured non-orthogonal walls, ceilings and floors of variable heights, twists and turns.  No longer would shooters be constrained to the square tile grids of the Greatest Generation and Silent Generation era shooter.

But something was sacrificed in that transition, and that was the simplicity of the tile, and consequently the speed of content creation and iteration. Building worlds out of tiles is incredibly simple and fast, and changing the world even faster.

*Tensor 1* seeks to recapture this simplicity, which allows it to come with a built-in tile-based level editor that anyone can use. Simply load up the editor, place a few tiles, hit play, and within seconds you can explore a world of your own creation.

For additional resources on using the tile-based level editor, see the official [game manual]({% link manual/editor/index.md %}).

### Physics

However, though the world is built on a tile structure, it also needs to feel feel as dynamic and interactive as the worlds of the classic Gen-X shooters of the late 1990s and early 2000s. To that end, *Tensor 1* makes extensive use of physics objects and interactions. *Tensor 1* uses the Bullet physics library for basic rigidbody calculations, along with custom written physics to constrain the behavior of certain key physics objects, and define the behavior of the force bow, one of the key tools in the player's arsenal.

### Artificial Intelligence

Of course, a dynamic world means more than just physics objects. The world also needs to be populated by dynamic monsters, powered by a flexible artificial intelligence (AI) system. *Tensor 1* makes use of two main types of AI, one for its hovering drones, and one for its infantry soldiers.

The AI of the hovering drones is primarily based on steering behavior. The drones regularly scan their surrounding area and applies a modifying force to its current velocity in order to chase its target while avoiding obstacles.

The soldier AI is more complex, intentionally modeled after the celebrated AI of one of the defining Gen-X shooters, Half-Life (1998). To that end, the soldier AI makes use of finite state machines (FSM), goals, tasks, and schedules. Added all together, the result is an AI that can find and take cover in response to player position, decide when to attack and when to retreat, flush the player out of their cover by deploying allied drones, and, if the player isn't careful enough, outflank and surprise the player.