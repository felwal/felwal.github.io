---
title: Acorn, Nocorn
summary: Critical design involving acorns, basket, and squirrel
team: [William Zhan]
assignment: For the course _DH2400 Physical Interaction Design_. The assignment was to "focus on the conceptual meaning" of the design; to be "critical, reflective, speculative and/or provocative."
role: I was responsible for coding and acorns, and except for the squirrel we worked on the rest together.
modified: 2024-12-14
started: 2024-02-19
completed: 2024-03-01
links:
  - Github: https://github.com/felwal-edu/dh2400
tags: [physical-interaction, critical-design]
tools: [arduino, cpp, processing]
series: [dh2400]
images: [acorn-nocorn-banner-2.png]
clusters: [acorn, dh2400, critical]
---

If you want the full experience, I recommend watching the video before reading further:

{{< gdrive 18_ujBFawAbg2ZIh1xvTFuaBtliJQCK8B >}}

The design consists of a birdhouse-like house where it is implied a squirrel lives, with an acorn visible at the entrance; a basket in which the acorns can be put; and a screen displaying the number of collected acorns. When all three acorns are collected, the floor opens and out falls the squirrel, committing suicide.

[It is based on the popular myth.]

## Conceptual meaning

Critical design is a method for challenging assumptions and norms, raising awareness, and sparking reflection.

Our design aims to make salient our very one-way relationship to the rest of nature as one of primarily _taking_. Stealing acorns from the squirrel is framed as _good_ – that's why we display the "You win!" message in the end, contrasting with the fact that this also means that somebody has to lose.

![](/images/acorn-nocorn-win.png)

There is little evidence of absolute decoupling between global economic growth and resource extraction,[^decouple] yet the narrative of "green growth" dominates. These things are complex, so we take a simple case: acorns (ecology) are directly transformed into points (economy). The squirrel dies as a direct consequence of the user's actions.

Yet we also use reductionist metrics and information-hiding to nudge the user towards our intended behaviour and to make the design more impactful: The counter incentivises stealing acorns (you get more of what you quantify), and the consequences are made clear only _after_ the fact.

## Process

We started with a long brainstorming session where we got a lot of ideas in the areas of critical, speculative, and more-than-human design. We decided on one, then started sketching different ways of realising the concept:

![](/images/acorn-nocorn-sketch.jpg)

I made the acorns out of Fimo clay and acrylics:

{{< figrow >}}
    {{< figure src="/images/acorns-3.jpg" >}}
    {{< figure src="/images/acorns.jpg" >}}
{{< /figrow >}}

[](/art/acorns)

And William made the squirrel through origami:[^origami]

{{< figrow force-row=true >}}
    {{< figure src="/images/acorn-nocorn-squirrel.jpg" >}}
    {{< figure src="/images/acorn-nocorn-squirrel-noose.jpg" >}}
{{< /figrow >}}

Then we got the UV sensor and servo motor to work with Arduino and Processing, and started on the props. We made the basket out of toilet paper roll with some thread glued on to give it the classic look, and attached the UV sensor in the box underneath to register falling acorns:

{{< figrow caption="**Right**: Arduino with connected servo motor and UV sensor" >}}
    {{< figure src="/images/acorn-nocorn-basket.jpg" >}}
    {{< figure src="/images/acorn-nocorn-wiring.jpg" >}}
{{< /figrow >}}

We made the house out of a cardboard box, with a hole for acorns (a tilted floor and a funnel made out of two sticks made sure they rolled out consistently), and a trapdoor closed by the servo:

![The final layout, from the back. The UV sensor is under the basket, hidden within the box. The servo motor keeps the house floor closed and the squirrel hidden.](/images/acorn-nocorn-back.jpg)

## Notes

[^origami]: Tutorial and design by Oriol Esteve: https://www.youtube.com/watch?v=tYO3IKW0vZo

[^decouple]: Parrique, T., Barth, J., Briens, F., Kerschner, C., Kraus-Polk, A., Kuokkanen, A., & Spangenberg, J. H. (2019). Decoupling debunked: Evidence and arguments against green growth as a sole strategy for sustainability. A study edited by the European Environment Bureau EEB, 3.
