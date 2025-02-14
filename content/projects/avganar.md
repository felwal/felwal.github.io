---
title: Avgånär
summary: Public transport widget for Garmin watches
published: 2025-01-26
modified: 2025-02-10
started: 2021-04-24
completed: 2024-06-16
released: 2022-11-26
weight: 1
links:
  - Github: https://github.com/felwal/avganar
  - Connect IQ Store: https://apps.garmin.com/apps/a96ddb52-3edd-4298-8348-5bd818376a2a
tags: [mobility]
tools: [garmin, monkeyc]
keytag: Product
images: [avganar-banner.png]
related: []
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

Developing for the Garmin ecosystem is ... not the best. Monkey C is like a combination of the worst parts of Java and Python. Layouts are calculated and drawn programatically. And developing for small round screens and limited memory was a challenge in itself.

The ecosystem is also very unstandardised, different watches having different layouts and styles. I settled on making it standard-compatible with one version of the OS, at the same time keeping a unique flair.

### Loading ...

A design challenge I encountered was indicating loading status without overriding the previous response with a "loading" message. Early user feedback made it clear that it was necessary to show in some way – but the standard "waiting for GPS" view didn't fit with my coloured panels. So I came up with this progress bar, integrated with the panels, indicating stage (GPS or API):

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-swe-stops-loading.png" >}}
    {{< figure src="/images/avganar-departures-loading.png" >}}
    {{< figure src="/images/avganar-departures-no-connection.png" >}}
{{< /figrow >}}

### Transport mode selection

At one point the API was updated to require requesting one mode at a time. As such I had to (within the migration span of one month) restructure and design an interaction for this:

![Exploring different ways to implement mode selection](/images/avganar-figma.png)

{{< figrow force-row=true caption="**Right**: before the menu, you would cycle through modes linearly" >}}
    {{< figure src="/images/avganar-modes.png" >}}
    {{< figure src="/images/avganar-swe-modes.png" >}}
    {{< figure src="/images/avganar-process-departures-train.png" >}}
{{< /figrow >}}

## What's next

I feel like this (seemingly simple) project has taken _way_ too much time. It's not the most exciting thing ever, yet it was instructive to finally release something. My plan for now is to mostly just maintain it with support for new watches.
