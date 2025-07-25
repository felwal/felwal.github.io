---
title: Spotify Librarian
summary: Redesign for AI-based music discovery
team: [William Rolf, Alexander Widman, William Zhan]
assignment: Serve music discovery behaviors using AI on new or existing surfaces, based on both implicit and explicit signals.
started: 2024-09-18
completed: 2024-12-20
role: UX, critical design; hifi individual extension of lofi group work
tags: [concept, critical-design, ai]
series: [dm2630]
keytag: UX
links:
    - Video: https://www.youtube.com/watch?v=35srVpMqtcM
images: [librarian-hero.png]
thumb: librarian-thumb.png
deviceHero: true
color: yellow
clusters: []
weight: 3
aliases: [librarian]
---

The Spotify Librarian is a personalised ape who helps you discover new music. It is inspired by Terry Pratchett's Discworld, and expands upon the metaphor of "Your Library".

### Ape Intelligence

AI has costs. The design tries to challenge the cornucopian paradigm by being ephemeral, making some of the material costs visible, and possibly making the user reconsider if they really need AI-recommendations right now. The Librarian has a life of their own and doesn't only exist to please the user.

### Music bananas

The explicit signal used is feeding the Librarian with music bananas representing specific songs. This mechanism also couples with the implicit signal – the amount of electricity available on the power grid – which determines how easy or hard it is to pull down and sling the music banana:

{{< devicerow force-row=true >}}
    {{< device src="/images/librarian-playing.gif" >}}
{{< /devicerow >}}

### Evolving taste and style

Feeding the Librarian affects their recommendations and look. Their taste is ephemeral: after a while their eaten music resets, and the style updates. The idea is to offer a more selective sandbox for music exploration. Librarian-recommended songs appear with the banana icon – in contrast to the (almost ideological) magic sparks:

{{< devicerow columns-mobile="2" >}}
    {{< device src="/images/librarian-open.png" >}}
    {{< device src="/images/librarian-open-v2.png" >}}
    {{< device src="/images/librarian-playlist.png" >}}
{{< /devicerow >}}

In this prototype they are images generated by DALL-E, but I would prefer something much simpler and cheaper, generating maybe costumes etc. applied to a predefined model.

### Hunger

The more hungry the Librarian is, the less precise their recommendations become. If completely empty, they become completely _random_. This is a way to vary back and forth on the scale of boring–too risky, instead of trying to home in on the "perfect" amount.

### Shadow Librarian

If the user instead feeds the Librarian too much, the recommendations instead flip to the _opposite_ of their learned taste. Here I use it to "punish" the user for spending too much electricity, water, etc. – yet it could at the same time help them discover music they never would have otherwise.

This is a playful take on the _Waluigi effect_: in teaching an AI model "good behavior", it also implicitly learns "bad behaviour".

![](/images/librarian-shadow.jpg)

Shadow or random recommendations might be considered a kind of breakdown, putting the user out of auto-pilot mode. Usability is only one of many values we can design for, and here I focussed more on creating a playful experience.

### Your Librarian found a friend!

Sometimes the Librarian ventures out into cyberspace and finds friends with similar taste:

{{< devicerow force-row=true >}}
    {{< device src="/images/librarian-friend.png" >}}
    {{< device src="/images/librarian-friend-v2.png" >}}
{{< /devicerow >}}

These are temporary and change when the taste changes, and their users are anonymous. This is to give it a more playful and less serious air, and have a semi-social feature that is consequential.

## Process

We started out with mapping how users currently discover new music, and then continued with HMWs and brainstorming:

![](/images/librarian-ideation.png)

After settling on and fleshing out an idea, we made a quick low-fi prototype in Miro:

{{< figrow force-row=true >}}
    {{< figure src="/images/librarian-process-closed.png" >}}
    {{< figure src="/images/librarian-process-open.png" >}}
    {{< figure src="/images/librarian-process-playlist.png" >}}
{{< /figrow >}}

Individually I started by exploring the feeding mechanism – I wanted it to be more unique and playful than a simple button:

![](/images/librarian-sketch.jpg)

## Related project: Stamped


{{< callout-group >}}
    {{< callout title="Brief" text="Design for _interdependence_" >}}
    {{< callout title="Team" text="Kristina Högberg, Edina Niculescu, Lennard Scheibel, Aikaterini Tsioutsia" >}}
    {{< callout text="Sep – Oct 2023" outline=true >}}
{{< /callout-group >}}

While the above project was very limited in scope, this course had a focus on the entire design process and its methods. We designed a mobile app fostering social activities and cultural exchange between new and old Stockholmers:

{{< devicerow columns-mobile="2" wide=true >}}
    {{< device src="/images/stamped-home.png" color="blue" >}}
    {{< device src="/images/stamped-events-focused.png" color="blue" >}}
    {{< device src="/images/stamped-view.png" color="blue" >}}
    {{< device src="/images/stamped-edit.png" color="blue" >}}
{{< /devicerow >}}

We performed interviews, cultural probe, personas, storyboards, affinity diagramming, insights extraction, how might we, brainstorming, brainwriting, parallel design, moodboard, and think-aloud.
