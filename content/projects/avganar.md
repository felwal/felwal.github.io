---
title: Avgånär
summary: Public transport widget for Garmin watches
published:
modified:
started: 2021-04-24
completed: 2024-06-16
released: 2022-11-26
weight: 1
links:
  - Github: https://github.com/felwal/avganar
  - Connect IQ Store: https://apps.garmin.com/apps/a96ddb52-3edd-4298-8348-5bd818376a2a
tags: [mobility, sustainability]
tools: [garmin, monkeyc]
images: [avganar-banner.png]
related: [projects/dh2400-toteometer]
---

Avgånär is a Garmin Connect IQ widget for viewing public transport nearby stops and departures. The base version works within Stockholm (SL) in Sweden, while a second version covers the entire Sweden.

It is perfect for checking when you need to leave home for the bus; or if you have to start running or can take it easy.

It's the first project I've released officially.

problem and motivation; autobiographical design

| ![](/images/avganar-glance.png) | ![](/images/avganar-preview.png) | ![](/images/avganar-stops-nearby.png) |
| - | - | - |

| ![](/images/avganar-stops-favorites.png) | ![](/images/avganar-modes.png) | ![](/images/avganar-departures-train.png) |
| - | - | - |

| ![](/images/avganar-departures-bus.png) | ![](/images/avganar-deviations.png) | ![](/images/avganar-error.png) |
| - | - | - |

If no favourites are set, the blue disappears. Some users found it unclear how to actually add favourites, so I added an explaining dialog-like view:

| ![](/images/avganar-stops-no-favs.png) | ![](/images/avganar-no-favs.png) | ![](/images/avganar-options.png) |
| - | - | - |

## Avgånär Sweden

Trafiklab also provides APIs for the entire Sweden, and I decided to create another version of the app implementing this. While it worked out alright in the end, I faced a number of challenges with this.

![](/images/avganar-swe-banner.png)

| ![](/images/avganar-swe-glance.png) |  ![](/images/avganar-swe-stops-nearby.png) | ![](/images/avganar-swe-stops-favorites.png)
| - | - | - |

| ![](/images/avganar-swe-modes.png) | ![](/images/avganar-swe-departures-train.png) | ![](/images/avganar-swe-error.png) |
| - | - | - |

First, the API responses were much bigger, and so for a departures response from a busy stop like Stockholm City barely worked at all with the extremely limited memory of the watches.

## What I've learnt

## Process

The watches developed for support down to only 64 colours. Fittingly, this is the quaternary colour space. It was fun to work with this limited palette – although the watch screen is not the best, meaning what looks good on a computer might not on the watch, and vice versa. This resulted in a lot of back-and-forth refinement. It also meant that the built-in colour constants were ill named: amber was called "yellow", and capri "blue". So of course I had to create my own mappings.

![](/images/quaternary-colors.png)

Color coding

| ![](/images/avganar-swe-group-color-explainer.png) | ![](/images/avganar-group-color-explainer.png) |
| - | - |

At the project's start, there existed no standard library for common components and widgets. (And even now, what has been released only works for newer devices.) Thus everything had to be calculated and drawn programatically.

When designing for a specific platform, it is important to follow its standards. The Garmin ecosystem however is quite unstandardised: different watches have different layouts, elements, and styles. As such I initially struggled with making the widget feel good. In the end I settled for adapting the lists and panels appearing consistently (enough) through the OS of the watch I own. I think I succeeded quite well in making it both standard-compatible and having a unique flair.

| ![](/images/garmin-sports.png) | ![](/images/garmin-sports-favorites.png) | ![](/images/garmin-connection.png) | ![](/images/garmin-activity-last.png) |
| - | - | - | - |

| ![](/images/garmin-activity-gps.png) | ![](/images/garmin-activity-menu.png) | ![](/images/garmin-dialog.png) |
| - | - | - |

One specific design challenge I encountered was how to indicate loading status. There are two stages: waiting for GPS, and waiting for API response. Early user feedback made it clear that this was necessary to show in some way – otherwise they would just ... wonder why the "nearby stops" didn't update. But I could't display a "loading" hint if there were already previously loaded stops; and the standard "waiting for GPS" view didn't fit with my coloured panels. And so I came up with the progress bar, integrated with the panels, indicating stage (GPS or API).

| ![](/images/avganar-swe-stops-loading.png) | ![](/images/avganar-departures-loading.png) | ![](/images/avganar-departures-no-connection.png) |
| - | - | - |

New API: limited departures per mode. Sweden response size

Here are some older iterations:

| ![](/images/avganar-process-departures-tram.png) | ![](/images/avganar-process-departures-train.png) | ![](/images/avganar-process-departures-too-large.png) |
| - | - | - |

splitting by mode

| ![](/images/avganar-modes.png) | ![](/images/avganar-swe-modes.png) |
| - | - |

Mode menu haptic feedback

Fitting everything

Balancing architecture with minimal computational resources

figma img

skisser imgs

## What's next

I feel like this (seemingly simple) project has taken _way_ too much time. It's not the most exciting thing ever, yet it was instructive to finally release something. My plan for now is to mostly just update it from time to time with support for new watches.

I also have some thoughts about developing for a niche platform like Garmin: Is it worth it? Post in progress.
