---
layout: page
title: Roadmap
permalink: /roadmap/
---

# Roadmap

This is a community-driven fan project with no deadlines. The roadmap shows milestones, not dates — items may be revisited or worked on concurrently based on development needs and community input.

Last update: 2025-11-16


## High-level overview

We’re prioritizing a first playable AI for Skirmish matches while continuing smaller work in parallel.

Planned milestones:

- Basic AI (for Skirmish and multiplayer matches)
- Gameplay mechanics
- Import legacy maps
- Single-player campaign
- Visual, audio and misc polish
- Classic/enhanced mode
- AI enhancements
- Possible brand new features

<div class="content">
    <a href="https://github.com/OpenE2140/OpenE2140/milestones" class="button is-dark">
        View milestones on GitHub
        <span class="icon is-small ml-1 has-text-grey-light">
            <i class="fas fa-arrow-right"></i>
        </span>
    </a>
</div>


## [Basic AI](https://github.com/OpenE2140/OpenE2140/milestone/8)

We’ll reuse OpenRA’s modular bot framework where possible, but due to the fact that OpenRA's AI is tailored to C&C games, several modules must be reimplemented for Earth 2140’s mechanics. Initial AI work will focus on core behaviors: base building, ore mining and technology research.


## [Gameplay mechanics](https://github.com/OpenE2140/OpenE2140/milestone/7)

Smaller gameplay and UI items need to be implemented to reach feature parity with the original game. These tasks are easy to split and can be completed between larger milestones.


## [Import legacy maps](https://github.com/OpenE2140/OpenE2140/milestone/11)

Multiplayer and single-player campaign maps need conversion into the OpenRA/OpenE2140 format. An importer will convert terrain, units/buildings, trees and other map objects to avoid manual recreation in the map editor.


## [Single-player campaign](https://github.com/OpenE2140/OpenE2140/milestone/9)

After maps are imported, campaign missions will be ported by extracting mission data (briefings, triggers, win/lose conditions) and adapting scripts to the new engine.


## [Visual, audio and misc polish](https://github.com/OpenE2140/OpenE2140/milestone/12)

General polish pass improving visuals, audio and miscellaneous systems to remove glitches and enhance overall quality.


## [Classic/enhanced mode](https://github.com/OpenE2140/OpenE2140/milestone/14)

OpenE2140 will offer two toggleable modes: "Classic" preserves the original game's behavior, while "Enhanced" enables optional modern improvements. Differences will be documented so players can choose their preferred experience.


## [AI enhancements](https://github.com/OpenE2140/OpenE2140/milestone/10)

AI will be iterated after the first playable version. Next steps include improving base construction and expansion, teaching the AI to use transporter units and build walls, and adding other gameplay behaviors (such as offensive/defensive AI generals).


## [New features to explore](https://github.com/OpenE2140/OpenE2140/milestone/15)

In the future we may experiment with new features that could improve overall experience of OpenE2140 beyond of what the original Earth 2140 offers.
