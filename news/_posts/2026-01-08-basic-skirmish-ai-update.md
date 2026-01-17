---
layout: post
title: "Skirmish AI update (January 2026)"
subtitle: "Long awaited update on Skirmish AI is here"
author: "OpenE2140 developers"
date: 2026-01-17
summary: "The development of the Skirmish AI is progressing well. In this post, we describe what implementing AI in OpenE2140 entails and where we currently stand in the process."
published: true
---

Since the Skirmish AI is the most requested feature for OpenE2140, we’ve decided to provide a status update on its development.

Creating AI for an RTS game is challenging, so we've opted to reuse as much logic from OpenRA as possible to speed up the development process.

### Current state

As of now, the basic AI for Skirmish in OpenE2140 is nearly complete. It can perform the following activities:

- Building a base and its defenses
- Collecting resources and managing the economy
- Researching technologies
- Constructing and managing an army
- Repairing buildings
- Building and utilizing superweapons

Overall, it serves as a fully competent opponent, capable of challenging human players. However, don't expect miracles; it is still an AI, and refinement is needed to smooth out rough edges. For instance, the bot occasionally stalls its unit production to expand its economy. Additionally, building placement can be suboptimal, as the AI sometimes positions structures too close to exits of production buildings or right next to conveyor belts of Mines or Refineries.

{% include video-embed.html title="Skirmish AI - Preview (1/2026)" src="https://dalek.zone/videos/embed/guign3e7XJcMRbSJue8jpM" %}

The video intentionally displays target lines for the orders the bots issue. This illustrates how the bots control their units, allowing you to observe their strategies before you compete against them.


### Bot modules

AI in OpenRA is modular, with AI players referred to as bots. Currently, we are using bot modules from the engine without modifications (though with custom configurations for OpenE2140) for the following features:

- Squad management
- Unit production
- Building repair
- Superweapons

Other modules provided by the engine cannot be applied because the game mechanics they are designed for operate differently in C&C games compared to Earth 2140 (and consequently in OpenE2140). These include:

- Base building
- Resource collection
- Capturing buildings
- Powering buildings down/up

(While powering buildings down/up is technically similar in both OpenE2140 and C&C games, the implementation differs, making the bot module for this mechanic incompatible with OpenE2140.)

Currently, we are working on the following necessary bot modules for a functional Skirmish AI in OpenE2140:

- Base building (using MCUs)
- Mining resources (using Mines/Refineries + Banthas/Heavy Lifters)
- Researching technologies

In the video below, you can see how base building and economy management are implemented. For this demo, unit production is disabled to make it easier to follow the actions of the AI bot. The bot also generates text notifications about its decisions, allowing you to observe its “thinking” in action.

{% include video-embed.html title="OpenE2140: AI base building (1/2026)" src="https://dalek.zone/videos/embed/rXUVw5K3thgyx5DkRwrbJc" %}

There’s also the Water Base, which hasn’t been mentioned yet. This building requires additional work, as it necessitates placing the Dock in water in addition to deploying the Water Base on shore. While we consider naval units core to the gameplay, naval warfare is currently not the focal point of OpenE2140. Thus, implementing it would delay the initial release of the Skirmish AI.

Bot modules and logic for these game mechanics will also be included at a later date, as they are not strictly necessary for a functional Skirmish AI:

- Staffing buildings with crew
- Capturing buildings (using armed or unarmed infantry or civilians)
- Constructing walls
- Properly utilizing Shadows/Screamers


### Next steps

Don’t expect these features soon, as we will be focusing on other essentials like remaining game mechanics and the single-player campaign. Check out [the roadmap]({% link roadmap.md %}) for a high-level view of our current work plan.

In general, it will take a lot of time to teach the AI to utilize all features and game mechanics available in OpenE2140. However, there’s no need to worry: eventually, everything from Earth 2140 will be implemented in OpenE2140, and it will function even better than the original game!


<div class="columns is-centered">
    <div class="column is-6">   
        {% include image-card.html image='images/news/2026-01-17-ai-superweapons.jpg' alt="Bots can use the deadly superweapons too." %}
    </div>
</div>


The basic Skirmish AI is coming soon, so stay tuned and follow us on [this website]({% link index.html %}), [Mod DB](https://www.moddb.com/mods/opene2140) or [GitHub](https://github.com/OpenE2140/OpenE2140).

If you haven't tried OpenE2140 yet, visit [the download page]({% link download.html %}), where you can find links to download the game and information on how to get it running.

We also have our own [Discord server](https://discord.gg/KNcX5BxA37), where you can chat with other OpenE2140 fans, connect with us, the developers, and even arrange multiplayer matches!

