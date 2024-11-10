---
layout: post
title:  "Feature Highlights"
date:   2024-11-11 12:00:00 -0700
categories: devlog
---

One of the central defining goals of *Tensor 1* is to combine the technical simplicty and elegance of the Greatest Generation/Silent Generation shooter with the narrative focus and world-building of the Generation X shooter [genres]({% post_url 2024-10-24-the-genre-of-tensor %}). In order to achieve this, *Tensor 1* focused on a five main pillars in its technology and design.

### Tile-Based World

The jump from the Greatest and Silent Generation era shooter to the Boomer shooter was marked by the release of Doom in 1993, which, among many other technical innovations, broke free of the square tile. Doom (1993) featured non-orthogonal walls, ceilings and floors of variable heights, allowing sprawling maps full of twists and turns.  No longer would shooters be constrained to the square tile grids of the Greatest Generation and Silent Generation era shooters like Wolfenstein 3D (1992).

But something was sacrificed in that transition, and that was the speed of content creation and iteration made possible by the simplicity of the square tile. Building worlds out of tiles is incredibly simple and fast, making creation and iteration fast. It is said that by the end of development, level designers working on Wolfenstein 3D could create an entire level in a single day.

*Tensor 1* seeks to recapture this ancient simplicity, which allows it to feature a built-in tile based level editor that anyone can use. Simply load up the editor, place a few tiles, hit play, and within seconds you can explore a world of your own creation.

For additional resources on using the tile-based level editor, see the official [game manual]({% link manual/editor/index.md %}) or reach out to [contact.magentagrid@gmail.com](mailto:contact.magentagrid@gmail.com) with questions, documentation requests, and feature requests.

### Physics

However, the danger of building a world out of tiles is that it can feel sterile and static, a serious problem for something trying to feel as dynamic and interactive as the worlds featured of the classic Gen-X shooters of the late 1990s and early 2000s. To that end, *Tensor 1* makes frequent use of interactive physics objects. *Tensor 1* uses the Bullet physics library for rigidbody calculations, along with custom written physics for the behavior of certain key physics objects, particularly the behavior of the force claw, one of the key tools in the player's arsenal. Progression through the world of *Tensor 1* requires mastery of the force claw and its ability to pull and push physics objects, whether to remove physical door locks, place a battery into an empty power slot, or throw an explosive drone back at the enemy soldier that deployed it.

### Artificial Intelligence

Of course, a dynamic world needs more than just physics objects. The world also needs to be populated by dynamic monsters, powered by a flexible artificial intelligence (AI) system. *Tensor 1* makes use of two main types of AI, one for its hovering drones, and one for its infantry soldiers.

The AI of the hovering drones is primarily based on steering behavior. The drones regularly scan their surrounding area and applies a modifying force to its current velocity in order to chase its target while avoiding obstacles.

The soldier AI is more complex, intentionally modeled after the celebrated AI systems featured in defining Gen-X shooters such as Half-Life (1998). To that end, the soldier AI makes use of finite state machines (FSM), goals, tasks, and schedules. In the simplest terms, the AI defines a goal, builds a schedule of tasks in order to achieve that goal, and then performs each task by traveling through the available states defined with the finite state machine. Added all together, the result is an AI that can find and take cover in response to player position, decide when to attack and when to retreat, flush the player out of their cover by deploying allied drones, and, if the player isn't careful enough, outflank and surprise the player.

### Multiplayer (Versus)

AI opponents, no matter how advanced, still cannot capture that special thrill of competing against another living, breathing, thinking person. For that reason *Tensor 1* comes with a competitive Local Area Network (LAN) multiplayer mode, a feature that was once almost universal during the era of Boomer and Gen-X shooters. In addition to Deathmatch and Team Deathmatch, *Tensor 1* multiplayer Versus mode includes a Capture the Flag mode where the flags are physics objects that players can grab and manipulate with the force claw.

### Controlled Randomization (Survival)

While the classic Boomer and Gen-X shooters of the late 1990s and early 2000s tended to include both single player and multiplayer components, from the age of Millenial shooter onward, 3D first person shooter games began to increasingly bifurcate into separate single player and multiplayer. Perhaps in our more modern age which is both more interconnected and more atomized, it is harder to enjoy and support multiplayer for small niche audiences. Most players instead gravitate toward large multiplayer-only focused games that can cultivate and support giant audiences.

Multiplayer games obviously provide replay value in the form of differing human players using differing strategies each game. For single player games chasing replay value, many turned to the example of Rogue (1980), a turn-based, grid-based role-playing game (RPG) based on exploring procedurally generated dungeons. Rogue initially spawned a subgenre of "Roguelikes," but developers working in other genres soon recognized the value of Roguelike randomization in creating replay value. They began to apply the randomization of Roguelikes to other genres, leading to the "Roguelike-like" or "Roguelite" genre.

In order to provide a source of replay value that does not depend on having to bug a friend to connect to through Versus mode, *Tensor 1* also includes Survival mode, which features the randomized run aspects of the Roguelite genre. In Survival mode, players go through a randomized sequence of levels, fighting off waves of enemies in the process. The spawning of enemy waves is partly random and partly managed by an AI Director system. The director program is put in place to control the difficulty ramp-up, seeking to strike the balance of offering up a challenge without overwhelming the player too quickly.
