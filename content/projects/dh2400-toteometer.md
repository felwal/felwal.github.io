---
title: Toteometer
summary: Tangible RGB color mixer, inspired by totems
published:
modified:
started: 2024-01-26
completed: 2024-02-02
links:
  - source: https://github.com/felwal-edu/dh2400
tags: [physical-interaction, totems]
tools: [arduino, cpp, processing]
series: [dh2400]
images: [toteometer-cover-2.png]
related: [/projects/dh2400-acorn-nocorn, /art/solartotem]
---

Design for the course DH2400 Physical interaction design. The assignment was to make "a working sensor that challenges the idea of a 'button' or that works in an unusual or unexpected way". _This text is an edited version of a hand-in for the course._

## Concept

This is the Toteometer, a tangible RGB color mixer inspired by totems. Here's a demonstration video:

{{< youtube 8JREaEHJSmU >}}

Totem parts are stacked to form totem poles. There are three spots on the base where a totem pole may be raised, corresponding to the primary colours red, green, and blue respectively. Depending on how many totem parts are stacked in each pole, a resulting colour is displayed on the computer screen. For example (as seen above), a three-high pole on G gives `#00FF00` (green); one on R and two on G gives `#55AA00` (dark orange); and one on each gives `#555555` (dark grey).

| ![](/images/toteometer-rgb.jpg) | ![](/images/toteometer-ggg.jpg) |
| - | - |

For the prototype I used Processing to display the colours, but the initial idea was to make it into a sort of lamp for ambient light, where the totem combination determined the colour of the light. As such it would have been a playful decoration, lamp, and interaction, all in one.

Initially I planned to make nine totem parts, which would allow mapping to all colours in the quaternary palette (white (`#FFFFFF`) requires three three-high poles):

![](/images/quaternary-colors.png)

Further, I would have liked to make it actually resemble totems, with the classic faces and wings and horns etc. from the original shamanic practices and popular media such as _Hearthstone_ and _Donkey Kong Country Returns_.

| ![](/images/totem-1.jpg) | ![](/images/totem-2.jpg) | ![](/images/totem-3.jpg) |
| - | - | - |

Time constrained these ideas, however; I had already spent 30 hours on the ten-hour project.

The idea of using totems originated from another project I'm brainstorming at the moment. Working with this adjacent design space has given me some new insights and inspiration – the explorations fuel each other, even though they're not directly linked.

[](/projects/permatotems)

## Process

I started out with a brainstorming session and then some background-level ideation over the next couple of days. When I had decided upon an idea, I began sketching the general design:

| ![](/images/toteometer-sketch-1.jpg) | ![](/images/toteometer-sketch-2.jpg) |
| - | - |

Next I had to figure out how the thing would actually work – at this stage I wasn't even certain if it could work at all. And so I took to re-learning the basic wiring stuff, realised it _could_ work, made a few failed attempts at sketching _how_ it would work, finally got it right, and then tried it out in Tinkercad.

I also did the math to figure out the optimal resistances in order to maximise the output span (to make calibration easier), and came to the conclusion that I needed two types, one twice as resistant as the other (left figure below). I started programming with Arduino and Processing, calculating the values which should correspond to zero, one, two, and three totem-high poles (right figure):

| ![](/images/toteometer-graph-vout-span.png) | ![](/images/toteometer-graph-vout.png) |
| - | - |

I made the totem parts out of Fimo clay and toilet paper rolls, then added wires, resistors, and aluminum (both on top and bottom) as connectors:

| ![](/images/toteometer-clay.jpg) | ![](/images/toteometer-wires.jpg) |
| - | - |

Oh, and those optimal resistances I calculated? After I had assembled these, I realised that they should have the higher resistance – _and_ that these, actually, were of the lowest possible resistance. And so the math was for nothing, and I ended up just hard-coding the values caused by each totem pole hight. Because these took some time to assemble.

And here's the base, made of a cardboard box, with wiring and aluminum:

![](/images/toteometer-box-open.jpg)

## Theory

In tangible interaction design, we can differentiate between tokens and constraints. In this design, the base contains three constraints: the three places where totems can be put. The totem parts themselves act both as manipulable loose tokens and as constraints for putting another totem part on top. The aluminum plates signify these constraints through the internal standard used in the project. Ideally I would have liked to make the affordances even better, with something like the stud and anti-stud of Lego bricks, as can be seen in the sketches above – though during the critique we agreed that the aluminum is probably good enough.

Victor [2021] defines four fundamental grips for hand manipulation. When the user interacts with the totem parts, they will likely use the _precision grip_. Victor contrasts our amazing manual capabilities with the paradigm of screens where we mostly just touch and swipe. When exploring the colour space of RGB and HEX on screens, I've noticed that it usually isn't very intuitive. That's a motivation for the Toteometer: making it tangible and discrete will allow the user to experiment and build embodied understandings.

## Discussion

During the critique we came up with a lot of ideas for other possible use cases for the mapping, such as:

- controlling the colour used in digital painting programs,
- mapping the number of people in different areas in a room to different lighting colours,
- a game where you combine ingredients to make a dish, or
- a design where you have to distribute your daily carbon quota between different domains (transport, consumption, etc.)

The totem parts turned out to be somewhat difficult to stack due to irregularities, something which made me a bit dissapointed at first. But someone in the crit realised that this _jiggliness_ needn't be a bad thing: maybe it could be a challenge, a balancing game!

If I made the totem parts into different figures actually looking like totems, it would bring a possible conflict: Would you stack them into the most attractive totem-combination, or in the combination resulting in the colour you want?

Finally, one might consider the use of totems as a form of appropriation, using only the surface-level looks of the shamanic practice, ignoring the underlying cultures and belief systems. In one way, this might resemble a _cargo cult_ as described by Holmquist [2005]. On the one hand, I think you should be able to be inspired by ideas in different cultures; on the other, the meta-culture of capitalism seems to systematically soak up all other cultures and worldviews as mere commodified trends.

## References

Holmquist, L. E. (2005). Prototyping: Generating ideas or cargo cult designs?. _Interactions_, _12_(2), 48-54.

Victor, B. (2021). A brief rant on the future of interaction design.
