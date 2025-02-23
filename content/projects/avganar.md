---
title: Avgånär
summary: Public transport widget for Garmin watches
published: 2025-01-26
modified: 2025-02-22
started: 2021-04-24
completed: 2024-06-16
released: 2022-11-26
links:
  - Github: https://github.com/felwal/avganar
  - Connect IQ Store: https://apps.garmin.com/apps/a96ddb52-3edd-4298-8348-5bd818376a2a
tags: [mobility]
tools: [garmin, monkeyc]
keytag: Product · App
images: [avganar-banner.png]
related: []
weight: 3
---

Avgånär is a Garmin watch widget for viewing nearby stops and departures at a glance. It is perfect for checking if you can stop stressing on your way to the bus – or if it's time to start running. The base version works within Stockholm (SL) in Sweden, while a second version covers the entire Sweden.

It's the first personal project I've released officially. After failing to finalise several Android apps, I wanted a smaller project and to focus on MVP principles. I started from a personal problem and employed autobiographical design, along with formative feedback from users.

## Overview

You can view nearby stops and add them as favorites:

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-glance.png" >}}
    {{< figure src="/images/avganar-stops-nearby.png" >}}
    {{< figure src="/images/avganar-stops-favorites.png" >}}
{{< /figrow >}}

Upcoming departures, filtered by transport mode:

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-modes.png" >}}
    {{< figure src="/images/avganar-departures-train.png" >}}
    {{< figure src="/images/avganar-departures-bus.png" >}}
{{< /figrow >}}

![](/images/avganar-irl.jpg)

Deviations and error handling:

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-deviations.png" >}}
    {{< figure src="/images/avganar-error.png" >}}
{{< /figrow >}}

### Avgånär Sweden

Trafiklab also provides APIs for the entire Sweden, and I decided to make another version of the app implementing this. The app is open source, so the idea is to be adaptable to other countries' public transport as well.

![](/images/avganar-swe-banner.png)

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-swe-glance.png" >}}
    {{< figure src="/images/avganar-swe-modes.png" >}}
    {{< figure src="/images/avganar-swe-departures-train.png" >}}
{{< /figrow >}}

## Process

The Garmin ecosystem is very unstandardised, with different watches having different layouts and styles. I settled on making it standard-compatible with one version of the OS, while at the same time keeping a unique flair.

### Mode selection

At one point the API was updated to require requesting one mode at a time. As such I had to (within the migration span of one month) restructure and design an interaction for this:

![Exploring different ways to implement mode selection](/images/avganar-figma.png)

{{< figrow force-row=true caption="**Right**: before the menu, you would cycle through modes linearly" >}}
    {{< figure src="/images/avganar-modes.png" >}}
    {{< figure src="/images/avganar-swe-modes.png" >}}
    {{< figure src="/images/avganar-process-departures-train.png" >}}
{{< /figrow >}}

## What's next

I feel like this (seemingly simple) project has taken _way_ too much time. It's not the most exciting thing ever, yet it was instructive to finally release something. My plan for now is to mostly just maintain it with support for new watches.

## Related projects: Trackfield and Markana

<p class="caption">Aug 2018 – Jan 2022</p>

I learned app design and development by building these Android apps. I never finished them due to a lack of MVP-strategy; lesson learnt the hard way.

Trackfield is for runs:

{{< figrow force-row=true >}}
    {{< figure src="/images/trackfield-exercises.png" >}}
    {{< figure src="/images/trackfield-view.png" >}}
    {{< figure src="/images/trackfield-edit.png" >}}
    {{< figure src="/images/trackfield-route.png" >}}
{{< /figrow >}}

And Markana is for Markdown notes:

{{< figrow force-row=true >}}
    {{< figure src="/images/markana-1.jpg" >}}
    {{< figure src="/images/markana-2.jpg" >}}
    {{< figure src="/images/markana-3.jpg" >}}
    {{< figure src="/images/markana-edit.jpg" >}}
{{< /figrow >}}
