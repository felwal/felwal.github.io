---
title: Escape Room
summary: Mobile multimodal puzzle-solving
team: [Prijun Koirala, Luca Lancella, William Zhan]
assignment: For the course _DT2140 Multimodal Interactions and Interfaces_.
role: Development of labyrinth, racing, and lock puzzles. Puzzle integration and Git coordination. Qualitative analysis.
published: 2025-02-09
modified: 2025-02-10
started: 2023-11-23
completed: 2024-01-10
tags: [xr]
tools: [unity, csharp, vuforia]
series: [dt2140]
keytag: AR · VR
images: [escaperoom-gyro-2.png]
weight: 5
---

In order to win the player completes four puzzles, collecting the codes and keys required to open the door and escape.

{{< youtube Qgya8fgqN-o >}}

### Tangibles

We used books as tangibles as they can be both handled with one hand and lay flat on a surface; the book cover can be used for image recognition; and most people have some at home. Interacting with the tangibles affects the AR environment.

### Meta puzzle

The Meta puzzle ties together all the other four puzzles with four locks. In accordance with the "open structure", they can be solved in any order:

{{< figrow >}}
    {{< figure src="/images/escaperoom-lock-1.png" >}}
    {{< figure src="/images/escaperoom-structure.jpg" outline=true >}}
{{< /figrow >}}

The two code locks use AR buttons with screen touch as input, while the two padlocks require keys attached to tangibles:

{{< figrow force-row=true >}}
    {{< figure src="/images/escaperoom-lock-pin-1.png" >}}
    {{< figure src="/images/escaperoom-lock-pin-2.png" >}}
    {{< figure src="/images/escaperoom-lock-key-1.png" >}}
    {{< figure src="/images/escaperoom-lock-key-2.png" >}}
{{< /figrow >}}

### Labyrinth puzzle

The labyrinth puzzle has the player tilting the book, getting the ball to the goal to receive a key:

{{< figrow force-row=true >}}
    {{< figure src="/images/escaperoom-gyro.png" >}}
    {{< figure src="/images/escaperoom-gyro-2.png" >}}
{{< /figrow >}}

While the ball is rolling, a looping audio track is played as feedback, with its speed and pitch modified dynamically as a function of the rolling speed.

### Racing puzzle

And for the racing puzzle you rotate the book like a wheel, steering a remote-controlled car to collect the key. Gas is applied through a traditional UI touch button. Touch was chosen as it is ubiquitous and contrasts with the untraditional tangible, to make the combination easier.

![](/images/escaperoom-racing.png)

## User evaluation

We performed a couple of think-aloud sessions coupled with interviews to evaluate the interactions and compare the different modalities. I handled the qualitative analysis, which included coding, affinity diagramming, and insights extraction:

{{< figrow >}}
    {{< figure src="/images/escaperoom-analysis-coding.png" >}}
    {{< figure src="/images/escaperoom-analysis-clustering.png" >}}
    {{< figure src="/images/escaperoom-analysis-insights.png" >}}
{{< /figrow >}}

Our main findings include:

- multitasking input modalities was difficult
- tangibles had unclear affordances but felt natural and immersive once learnt
- puzzle order affected learning of how to interact with untraditional modalities

## Related project: VR Urban Stress Mapping

<p class="caption">Dec 2023 – Jan 2024</p>

In this VR study we designed a city and examined the impact of environmental variables on perceived stress – including cold vs warm light:

![](/images/urban-stress-warm-vs-cold.png)

And three different levels of vegetation with accompanying sounds:

{{< figrow >}}
    {{< figure src="/images/urban-stress-vegetation-high.png" >}}
    {{< figure src="/images/urban-stress-vegetation-medium.png" >}}
    {{< figure src="/images/urban-stress-vegetation-none.png" >}}
{{< /figrow >}}

Natural elements and sounds had a calming effect, while lighting preferences were mixed.

{{< callout-group >}}
    {{< callout title="Assignment" text="Demo and study for the course _DM2350 Human Perception for IT_." >}}
    {{< callout title="Team" text="Carl Holmqvist, Pranit Popli, William Rolf, Alexander Widman" >}}
{{< /callout-group >}}
