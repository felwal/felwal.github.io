---
title: Avgånär
summary: Public transport widget for Garmin watches
published: 2025-01-26
modified:
started: 2021-04-24
completed: 2024-06-16
released: 2022-11-26
weight: 1
links:
  - Github: https://github.com/felwal/avganar
  - Connect IQ Store: https://apps.garmin.com/apps/a96ddb52-3edd-4298-8348-5bd818376a2a
tags: [mobility]
tools: [garmin, monkeyc]
images: [avganar-banner.png]
related: [projects/toteometer]
---

Avgånär is a Garmin watch widget for viewing nearby stops and departures at a glance. It is perfect for checking if you can stop stressing – or if it's time to start running. The base version works within Stockholm (SL) in Sweden, while a second version covers the entire Sweden.

It's the first project I've released officially. After failing to finalise several Android apps, I wanted a smaller project and to focus on MPV principles. I started from a personal problem and employed autobiographical design, along with formative feedback from users.

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-glance.png" >}}
    {{< figure src="/images/avganar-preview.png" >}}
    {{< figure src="/images/avganar-stops-nearby.png" >}}
{{< /figrow >}}

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-stops-favorites.png" >}}
    {{< figure src="/images/avganar-modes.png" >}}
    {{< figure src="/images/avganar-departures-train.png" >}}
{{< /figrow >}}

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-departures-bus.png" >}}
    {{< figure src="/images/avganar-deviations.png" >}}
    {{< figure src="/images/avganar-error.png" >}}
{{< /figrow >}}

## Avgånär Sweden

Trafiklab also provides APIs for the entire Sweden, and I decided to create another version of the app implementing this.

![](/images/avganar-swe-banner.png)

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-swe-glance.png" >}}
    {{< figure src="/images/avganar-swe-stops-nearby.png" >}}
    {{< figure src="/images/avganar-swe-stops-favorites.png" >}}
{{< /figrow >}}

{{< figrow force-row=true >}}
    {{< figure src="/images/avganar-swe-modes.png" >}}
    {{< figure src="/images/avganar-swe-departures-train.png" >}}
    {{< figure src="/images/avganar-swe-error.png" >}}
{{< /figrow >}}

## What's next

I feel like this (seemingly simple) project has taken _way_ too much time. It's not the most exciting thing ever, yet it was instructive to finally release something. My plan for now is to mostly just update it from time to time with support for new watches.
