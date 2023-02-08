---
layout: post
title:  "Introducing Arête"
author: "James Ordner"
date:   2023-02-07 10:46:59 -0900
categories: news
---
After years of tinkering and research, I am thrilled to announce **Arête**!

Arête aspires simply to be the fastest multiplatform, general-purpose game engine on the planet.

The traditional approach to game engine architecture is leaving more and more to be desired. CPUs and GPUs have continued to become faster and ever more integrated, and yet game engines have been slow to adapt to the capabilities of modern hardware. Desktops with discrete GPUs and the growing market share of fully-integrated systems (mobile devices, Apple Silicon, many Windows laptops, consoles, and VR headsets) both stand to benefit hugely from a new approach to game engine design. Arête introduces a revolutionary architecture which does exactly this.

Arête aims to support all of the features expected of modern engines. Full 2D and 3D rendering pipelines, robust audio systems, networking, UI, level editing and asset management tools… in short, Arête is not a barebones framework, but a fully-fledged engine aiming to compete with the likes of Unity and Unreal Engine. But what sets Arête apart is not its feature parity with existing game engines. What sets Arête apart is how it is able to offer feature parity with these engines while achieving unprecedented performance.

**How unprecedented?**

In order to generate some numbers, I took Unity’s [DOTS tutorial][DOTS-tutorial] and replicated it 1:1 in Arête. No shortcuts were taken: objects follow the same parenting hierarchy, the same meshes are loaded at runtime, and the simulation code matches Unity’s code exactly. Because the entity spawn rate in the tutorial is tied to the framerate, I capped entity spawning to 64k in both engines in order to maintain an accurate comparison.

Being a part of the Rust community, I’m sure Arête will also draw comparisons to [Bevy][bevy]. I personally take a lot of inspiration from Bevy’s ease-of-use and ergonomics, but the performance speaks for itself.

<p style="text-align: center;"><b>Average CPU Frame Time (milliseconds, less is better)</b></p>
<img src="/assets/posts/2023-02-07/frametime.svg" style="display: block; margin: 0 auto">

That's 64k entities at 920μs per frame with CPU culling and *110μs* per frame with GPU culling. 🤯

**Okay, so Arête is fast. *Really* fast.** But is that really compelling enough to take on the big players? It seems like raw performance is the main selling point of Arête.

I believe that the answer is *yes absolutely*. Performance doesn’t just help you meet your framerate targets or allow hardcore gamers to run your game at extreme framerates. Performance gives you the freedom to add new features to your game that weren’t previously possible, bring cutting-edge experiences to a wider audience (looking at you, mobile), and allow longer play sessions and avoid thermal throttling on battery-powered devices. **In short, you gain access to a larger market without cutting corners, and increase your value within your existing market.** And all else equal, what developer wouldn’t choose the faster of two game engines?

At this point, I hope that you’re half as excited about Arête as I am. There’s still a lot of work to be done and features to implement, but I’ve proven that the fundamental design is going to work, and it works well.

So why announce Arête before it’s ready to share?

I have big plans for Arête. I believe its architecture is revolutionary and has the potential to make it a major player in the game engine market. But to achieve that, I need the support of a dedicated team of talented people. To build a team, I need investment. And for that, I need to prove that Arête is something worth getting excited about.

Starting today, I will begin posting regular updates on Arête’s progress. My focus will shift from being 100% dedicated to development to splitting my time between development, publicity, and reaching out to investors. The question is no longer *will it work*, but *how fast can I get this out into the world*, and nothing will speed Arête’s development more quickly than building a team around it.

If you are excited about Arête, there are ways you can help out! At this stage, the most important action item is to build some hype around the project. Sharing this post around the gamedev community would provide a massive boost to the project, generate discussion and influence the direction of Arête, and increase the chances of investment in (and thus development of) the project. You can also [join the community on Discord][discord]!

If you are interested in joining the team, please don’t hesitate to reach out.

**Here’s to an exciting future!**

James

[DOTS-tutorial]: https://github.com/Unity-Technologies/EntityComponentSystemSamples/tree/master/EntitiesSamples/EntitiesTutorial
[bevy]: https://bevyengine.org/
[discord]: https://discord.gg/hRQSxztaFP
