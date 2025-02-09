---
title: Toteometer
summary: Tangible RGB color mixer, inspired by totems
modified: 2024-12-14
started: 2024-01-26
completed: 2024-02-02
links:
  - Github: https://github.com/felwal-edu/dh2400
tags: [physical-interaction]
tools: [arduino, cpp, processing]
series: [dh2400]
clusters: [totems, dh2400]
images: [toteometer-cover-2.png]
weight: 1
---

Prototype for the course DH2400 Physical Interaction Design. The assignment was to make "a working sensor that challenges the idea of a 'button' or that works in an unusual or unexpected way".

Totem parts are stacked to form totem poles. There are three spots where a totem pole may be raised, corresponding to the primary colours red, green, and blue. Depending on how many totem parts are stacked in each pole, a resulting colour is displayed on the computer screen.

The user explores the (usually pretty unintuitive) RGB and HEX colour space in a tangible and discrete way, which allows for experimentation and building embodied understandings.

{{< youtube 8JREaEHJSmU >}}

{{< figrow force-row=true caption="`#5A0` dark orange; `#0F0` green; `#555` dark grey" >}}
    {{< figure src="/images/toteometer-dark-orange.jpg" >}}
    {{< figure src="/images/toteometer-green.jpg" >}}
    {{< figure src="/images/toteometer-dark-grey.jpg" >}}
{{< /figrow >}}

## Further development

I would have liked to make the parts actually resemble totems, with the classic faces and wings and horns etc. from the original shamanic practices and popular media such as _Hearthstone_ and _Donkey Kong Country Returns_. This idea came from another project I'm working on – and exploring this adjacent design space has facilitated additional inspiration and insights.

{{< figrow force-row=true caption="Kia'palano totems, Vancouver" >}}
    {{< figure src="/images/totem-1.jpg" >}}
    {{< figure src="/images/totem-2.jpg" >}}
{{< /figrow >}}

I would also make the affordances better, with something like the stud/anti-stud of Lego bricks, as can be seen in the sketches further down.

[Modular figurine utilising the stud/anti-stud technique](/art/solartotem)

I used Processing to display the colours on screen, but the initial idea was to make it into a sort of lamp for ambient light. As such it would have been a playful decoration, lamp, and interaction, all in one. Though I only made three totem parts for the prototype, with nine it would be possible to map all colours in the quaternary palette:

![](/images/quaternary-colors.png)

## Process

I started out with a brainstorming session and some background-level ideation over a couple of days. When I had decided upon an idea, I began sketching the general design:

{{< figrow force-row=true >}}
    {{< figure src="/images/toteometer-sketch-1.jpg" >}}
    {{< figure src="/images/toteometer-sketch-2.jpg" >}}
{{< /figrow >}}

Next I had to figure out how the thing would actually work – at this stage I wasn't even certain if it could work at all. And so I took to re-learning basic electronics and wiring, realised it _could_ work, made a few failed attempts at sketching _how_ it would work, finally got it right, and then tried it out in Tinkercad.

I also did the math to figure out the optimal resistances in order to maximise the output span and make calibration easier:

{{< figrow force-row=true caption="Left: Signal output span as a function of the ratio between the resistances. Right: Signal strengths by all possible totem heights." >}}
    {{< figure src="/images/toteometer-graph-vout-span.png" outline=true >}}
    {{< figure src="/images/toteometer-graph-vout.png" outline=true >}}
{{< /figrow >}}

I made the totem parts out of Fimo clay and toilet paper rolls, then added wires, resistors, and aluminum as connectors:

{{< figrow >}}
    {{< figure src="/images/toteometer-clay.jpg" >}}
    {{< figure src="/images/toteometer-wires.jpg" >}}
{{< /figrow >}}

And here's the base, made of a cardboard box, with wiring and aluminum:

![](/images/toteometer-box-open.jpg)
