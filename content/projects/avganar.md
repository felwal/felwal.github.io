---
title: Avgånär
summary: Public transport widget for Garmin watches
published: 2025-01-26
modified: 2025-02-24
started: 2021-04-24
completed: 2024-06-16
released: 2022-11-26
links:
  - Github: https://github.com/felwal/avganar
  - Connect IQ Store: https://apps.garmin.com/apps/a96ddb52-3edd-4298-8348-5bd818376a2a
tags: [mobility]
tools: [garmin, monkeyc]
keytag: Product · App
images: [avganar-hero.png]
deviceHero: true
color: blue
related: []
weight: 1
aliases: [apps, appdev]
---

Avgånär is a Garmin watch widget for viewing nearby stops and departures at a glance. It is perfect for checking if you can stop stressing on your way to the bus – or if it's time to start running. The base version works within Stockholm (SL) in Sweden, while a second version covers the entire Sweden.

It's the first personal project I've released officially. After failing to finalise several Android apps, I wanted a smaller project and to focus on MVP principles. I started from a personal problem and employed autobiographical design, along with formative feedback from users.

## Overview

You can view nearby stops and add them as favorites:

{{< devicerow columns-mobile="2" >}}
    {{< device src="/images/avganar-glance.png" form="watch" >}}
    {{< device src="/images/avganar-stops-nearby.png" form="watch" >}}
    {{< device src="/images/avganar-stops-favorites.png" form="watch" >}}
{{< /devicerow >}}

Upcoming departures, filtered by transport mode:

{{< devicerow columns-mobile="2" >}}
    {{< device src="/images/avganar-modes.png" form="watch" >}}
    {{< device src="/images/avganar-departures-train.png" form="watch" >}}
    {{< device src="/images/avganar-departures-bus.png" form="watch" >}}
{{< /devicerow >}}

![](/images/avganar-irl.jpg)

Deviations and error handling:

{{< devicerow force-row=true >}}
    {{< device src="/images/avganar-deviations.png" form="watch" >}}
    {{< device src="/images/avganar-error.png" form="watch" >}}
{{< /devicerow >}}

### Avgånär Sweden

I decided to make another version of the app for the entire Sweden. The app is open source, so the idea is to be adaptable to other countries' public transport as well.

{{< devicerow wide=true columns-mobile="2" >}}
    {{< device src="/images/avganar-swe-glance.png" form="watch" color="green" >}}
    {{< device src="/images/avganar-swe-stops-nearby.png" form="watch" color="green" >}}
    {{< device src="/images/avganar-swe-modes.png" form="watch" color="green" >}}
    {{< device src="/images/avganar-swe-departures-train.png" form="watch" color="green" >}}
{{< /devicerow >}}

## Process

The Garmin ecosystem is very unstandardised, with different watches having different layouts and styles. I settled on making it standard-compatible with one version of the OS, while keeping a unique flair.

### Mode selection

At one point the API was updated to require requesting one transport mode at a time. As such I had to restructure and design an interaction for this:

![Exploring different ways to implement mode selection](/images/avganar-figma.png)

{{< devicerow force-row=true caption="**Right**: before the menu, you would cycle through modes linearly" >}}
    {{< device src="/images/avganar-modes.png" form="watch" >}}
    {{< device src="/images/avganar-swe-modes.png" form="watch" color="green" >}}
    {{< device src="/images/avganar-process-departures-train.png" form="watch" >}}
{{< /devicerow >}}

## What's next

This seemingly simple project is not the most exciting thing ever – yet it was instructive to finally release something with all that that entails, including legal and support. My plan for now is to mostly just maintain it with support for new watches.

## Related projects: Trackfield and Markana

<p class="caption">Aug 2019 – Jan 2022</p>

I learned app design and development by building these Android apps. I never finished them due to a lack of MVP-strategy; lesson learnt the hard way.

Trackfield is for runs:

{{< devicerow columns-mobile="2" wide=true >}}
    {{< device src="/images/trackfield-exercises.png" color="green" >}}
    {{< device src="/images/trackfield-view.png" color="green" >}}
    {{< device src="/images/trackfield-edit.png" color="green" >}}
    {{< device src="/images/trackfield-route.png" color="green" >}}
{{< /devicerow >}}

And Markana is for Markdown notes:

{{< devicerow columns-mobile="2" wide=true >}}
    {{< device src="/images/markana-1.jpg" color="pink" form="phone-old" >}}
    {{< device src="/images/markana-2.jpg" color="pink" form="phone-old" >}}
    {{< device src="/images/markana-3.jpg" color="pink" form="phone-old" >}}
    {{< device src="/images/markana-edit.jpg" color="pink" form="phone-old" >}}
{{< /devicerow >}}
