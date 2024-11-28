---
title: Acorn, Nocorn
summary: Critical design involving acorns, basket, and squirrel
modified:
started: 2024-02-19
completed: 2024-03-01
links:
  - source: https://github.com/felwal-edu/dh2400
tags: [physical-interaction, critical-design, sustainability]
tools: [arduino, cpp, processing]
series: [dh2400]
images: [acorn-nocorn-cover.png]
clusters: [acorn]
related: [/projects/dh2400-toteometer]
---

Co-design with William Zhan for the course DH2400 Physical interaction design. The assignment was to "focus on the conceptual meaning" of the design; to be "critical, reflective, speculative and/or provocative." _This text is an edited version of a hand-in for the course._

## Concept and theory

Acorn, Nocorn is a critical design, co-designed with William Zhan. I recommend watching the video before reading further:

{{< gdrive 18_ujBFawAbg2ZIh1xvTFuaBtliJQCK8B >}}

The design consists of a birdhouse-like house in which it is implied a squirrel lives, with an acorn visible at the entrance; a basket in which the acorns can be put; and the screen displaying the amount of collected acorns.

***

Critical design is a method for challenging assumptions and norms, raising awareness of the concequences of our actions, and sparking reflection and discussion.

Our design aims to make salient our very one-way relationship to the rest of nature as one of primarily _taking_. Stealing acorns from the squirrel is framed as _good_ – for you, for the economy, for humanity. That's why we display the "You win!" message in the end, contrasting what is usually deemed universally good with the fact that this also means that somebody has to lose:

![](/images/acorn-nocorn-win.png)

The global economy is so complex that any suggested link between it growing and global ecosystems failing is met with skepticism. Our design takes a simple case: acorns (ecology) are directly transformed into points (economy). From this point of view, "green growth" might be seen as _still taking_, but in a nicer (?) way. Chances are you wouldn't even consider it "stealing". That's another thing we thought a lot about during ideation: We have our systems and they have theirs, yet we only consider our own as legitimate. These systems overlap in messy ways, and we often ignore them or consider only ourselves as legitimate actors; we are very system-centric.

This simple case shows the squirrel dying as a direct consequence of the user's actions. It makes the consequences _visible_, in contrast to the information-hiding of mass-production. Fernaeus and Lindegren [2023] argue that we should acknowlegde and celebrate complexity and imperfection, because only then can we start improving on it. Yet our design also makes use of reductionist metrics and information-hiding in order to nudge the user towards our intended behaviour, and to make the design more impactful: The counter incentivises stealing acorns (you get more of what you quantify [Meadows 2008]), and the consequences are made clear only _after_ the fact.

## Process

We started with a looong brainstorming session where we got a lot of ideas in the areas of critical, speculative, and more-than-human design. We decided on one, then started sketching different ways of realising the concept:

![](/images/acorn-nocorn-sketch.jpg)

I made the acorns out of Fimo clay and acrylics:

| ![](/images/acorns-3.jpg) | ![](/images/acorns.jpg) |
| - | - |

[](/art/acorns)

And William made the squirrel through origami:

| ![Following the tutorial by Oriol Esteve [^origami]](/images/acorn-nocorn-squirrel.jpg) | ![](/images/acorn-nocorn-squirrel-noose.jpg) |
| - | - |

[^origami]: Tutorial and design by Oriol Esteve: https://www.youtube.com/watch?v=tYO3IKW0vZo

Here are some images used as inspiration and reference:

| !["Squirrel house" by shaunstreeper [^house]](images/shaunstreeper-squirrel-house.jpg)| !["Mushroom Basket" by cwasteson [^basket]](images/cwasteson-mushroom-basket.jpg) | !["Acorn" by randihausken [^acorn]](images/randihausken-acorn.jpg) |
| - | - | - |

[^house]: "[Squirrel house](https://www.flickr.com/photos/141992429@N08/52380699715)" by shaunstreeper, licensed under [CC BY-NC 2.0](https://creativecommons.org/licenses/by-nc/2.0/)

[^basket]: "[Mushroom Basket](https://www.flickr.com/photos/46202322@N03/6016784701)" by cwasteson, licensed under [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/)

[^acorn]: "[Acorn](https://www.flickr.com/photos/46406832@N00/2881856339)" by randihausken, licensed under [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/)

Then we got the UV sensor and servo motor to work with Arduino and Processing, and started on the props. We made the basket out of toilet paper roll with some thread glued on to give it the classic look, and attached the UV sensor in the box underneath to register falling acorns:

| ![](/images/acorn-nocorn-basket.jpg) | ![Arduino with connected servo motor and UV sensor](/images/acorn-nocorn-wiring.jpg) |
| - | - |

We made the house out of a cardboard box, with a hole for acorns (a tilted floor and a funnel made out of two sticks made sure they rolled out consistently), and a trapdoor closed by the servo:

![The final layout, from the back. The UV sensor is under the basket, hidden within the box. The servo motor keeps the house floor closed and the squirrel hidden.](/images/acorn-nocorn-back.jpg)

For audio effects we used the _Super Mario_ coin sound for feedback on collecting the acorns. We also used the rabbit death sound from _Minecraft_, since there (surprisingly) are no squirrels in that game.

## Discussion

In our haste to get the design finished on time, and due to having borrowed an Arduino, we did not have any third party test the design. It would have been really fun and insightful to see people's behaviours and reactions in real-time, compared to just showing the video.

During the critique we discussed whether the design is _desirable_. For whom? How to define "desirable"? It's (hopefully) a bit uncomfortable – so, emotionally, no? But then it might make you think about things you hadn't before – so, intellectually, yes? From the wider perspective of civilisation, we need to reconsider our relationship with the rest of nature – so, ecologically, yes?

And for the squirrels? They are just the unknowing, nonconsenting objects of our cruel joke.

## References

Fernaeus, Y., & Lindegren, A. (2023). Celebration of finitude as a post-industrial aesthetics of interaction. In _LIMITS_.

Meadows, D. H. (2008). _Thinking in Systems: A primer_. Chelsea green publishing.
