---
title: AR Escape Room
summary: Mobile multimodal puzzle-solving
team: [Prijun Koirala, Luca Lancella, William Zhan]
started: 2023-11-23
completed: 2024-01-10
role: AR development, user evaluation, qualitative analysis
links:
    - Video: https://www.youtube.com/watch?v=Qgya8fgqN-o
tags: [xr]
tools: [Unity, C#, Vuforia]
series: [dt2140]
keytag: XR
images: [escaperoom-hero.png]
thumb: escaperoom-thumb.png
deviceHero: true
color: blue
weight: 5
aliases: [escaperoom]
---

In order to win the player completes four puzzles, collecting the codes and keys required to open the door and escape. We used books as tangibles as they can be handled with one hand, be used for image recognition, and most people have some at home.

{{< devicerow columns-mobile="2" wide=false >}}
    {{< device src="/images/escaperoom-lock.png" >}}
    {{< device src="/images/escaperoom-gyro.png" >}}
    {{< device src="/images/escaperoom-racing.png" >}}
{{< /devicerow >}}

### Meta puzzle

The Meta puzzle ties together all the other four puzzles with four locks. In accordance with the "open structure", they can be solved in any order. The two code locks use AR buttons with screen touch as input, while the two padlocks require keys attached to tangibles:

{{< figrow columns-mobile="2" wide=true >}}
    {{< figure src="/images/escaperoom-lock-pin-1.png" >}}
    {{< figure src="/images/escaperoom-lock-pin-2.png" >}}
    {{< figure src="/images/escaperoom-lock-key-1.png" >}}
    {{< figure src="/images/escaperoom-lock-key-2.png" >}}
{{< /figrow >}}

### Labyrinth puzzle

The labyrinth puzzle has the player tilting the book, getting the ball to the goal to receive a key:

{{< gdrive 1hfhvaB-gZv6BSobYABD7ZV6sCQotY8UW >}}

### Racing puzzle

And for the racing puzzle you rotate the book like a wheel, steering a remote-controlled car to collect the key. Gas is applied through a traditional GUI touch button.

{{< gdrive 1WswlOjJQp9du3tou2WqsYbkYu8PDn-Y0 >}}

## User evaluation

We performed a couple of think-aloud sessions coupled with interviews to evaluate the interactions and compare the different modalities. I handled the qualitative analysis, which included coding, affinity diagramming, and insights extraction:

{{< figrow force-row=true wide=true >}}
    {{< figure src="/images/escaperoom-analysis-clustering.png" outline=true >}}
    {{< figure src="/images/escaperoom-analysis-insights.png" outline=true >}}
{{< /figrow >}}

Our main findings include:

- multitasking input modalities was difficult
- tangibles had unclear affordances but felt natural and immersive once learnt
- puzzle order affected learning of how to interact with untraditional modalities

## Related project: VR Urban Stress Mapping

{{< callout-group >}}
    {{< callout title="Team" text="Carl Holmqvist, Pranit Popli, William Rolf, Alexander Widman" >}}
    {{< callout text="Dec 2023 – Jan 2024" outline=true >}}
{{< /callout-group >}}

In this VR study we designed a city and examined the impact of environmental variables on perceived stress – including cold vs warm light:

![](/images/urban-stress-warm-vs-cold.png)

And three different levels of vegetation with accompanying sounds:

{{< figrow >}}
    {{< figure src="/images/urban-stress-vegetation-high.png" >}}
    {{< figure src="/images/urban-stress-vegetation-medium.png" >}}
    {{< figure src="/images/urban-stress-vegetation-none.png" >}}
{{< /figrow >}}

We found that natural elements and sounds had a calming effect, while lighting preferences were mixed.
