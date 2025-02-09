---
title: AR Escape Room
summary: Mobile AR game where the player solves puzzles to escape
team: [Prijun Koirala, Luca Lancella, William Zhan]
assignment: For the course _DT2140 Multimodal Interactions and Interfaces_.
role: I made the labyrinth and racing puzzles, helped out with the locks, managed puzzle integration and Git coordination, and performed the qualitative analysis.
published: 2025-02-09
modified:
started: 2023-11-23
completed: 2024-01-10
tags: [xr]
tools: [unity, csharp, vuforia]
series: [dt2140]
images: [escaperoom-gyro-2.png]
---

In order to win the player completes four puzzles, collecting the codes and keys required to open the door and escape.

We used books as tangibles as they can both be handled with one hand and lay flat on a surface, and since the book cover can be used for image recognition.

{{< youtube Qgya8fgqN-o >}}

### Lock puzzle

There are four locks corresponding to the four puzzles:

{{< figrow force-row=true >}}
    {{< figure src="/images/escaperoom-lock-pin-1.png" >}}
    {{< figure src="/images/escaperoom-lock-pin-2.png" >}}
    {{< figure src="/images/escaperoom-lock-key-1.png" >}}
    {{< figure src="/images/escaperoom-lock-key-2.png" >}}
{{< /figrow >}}

![](/images/escaperoom-lock-1.png)

### Gyro puzzle

The gyro puzzle has the player tilting the book, getting the ball to the goal to receive a key:

{{< figrow force-row=true >}}
    {{< figure src="/images/escaperoom-gyro.png" >}}
    {{< figure src="/images/escaperoom-gyro-2.png" >}}
{{< /figrow >}}

### Racing puzzle

And for the racing puzzle you turn the book like a wheel, steering a small car:

![](/images/escaperoom-racing.png)

## User evaluation

We performed a couple of think-out-loud sessions coupled with interviews to evaluate the interactions and compare the different modalities.

I handled the analysis, which included coding:

![](/images/escaperoom-analysis-coding.png)

Affinity diagramming:

![](/images/escaperoom-analysis-clustering.png)

And insights extraction:

![](/images/escaperoom-analysis-insights.png)
