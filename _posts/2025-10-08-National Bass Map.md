---
layout: post
title: 🔺 National Bass Map
---

I recently came across the excellent work done by the [National Bass Directory](https://nationalbassdirectory.wordpress.com/). A pdf of pubs serving Bass, updated monthly with tip offs from regular drinkers (Bassketeers). However, no one had gone to the trouble of putting them in a Google map layer for easy navigation. This was fairly easily remedied. You can find the map [here](https://www.google.com/maps/d/edit?mid=1pgF_A7wvn17yKz4KNUWqZZ62fl7Rfa8&usp=sharing), and the code that made it [here](https://github.com/fred-cook/Bass-map).

The code runs every morning at ~9am (Github cron jobs are dependent on when a runner becomes available) and tags me in a comment if there are any changes to the pub locations csvs. If there are, I upload them manually to the google map layer. A future job may be to automate this entirely, but I think I will need to host the data somewhere myself.

The Bass directory adds several useful bits of information, whether it is guest or permanent, when it was last sighted, the pouring method ([banked bass](https://www.pelliclemag.com/home/2022/4/6/i-want-to-see-mountains-again-the-banked-beers-of-teesside-north-east-england)🤤) and any other notes. Visually the map separates permanent and guest locations.


| Permanent bass symbol | Guest bass symbol |
|:--|:--|
| <img src="https://github.com/fred-cook/Bass-map/blob/main/images/permanent_logo.png?raw=true" alt="Permanent bass symbol" width="220" /> | <img src="https://github.com/fred-cook/Bass-map/blob/main/images/guest_logo.png?raw=true" alt="Guest bass symbol" width="220" /> |


Suggestions for improvements on the map/production process welcome! If you have a Bass sighting near you that's not on the list report it on the [Facebook group](https://www.facebook.com/groups/nationalbassday) or in the comments section of the latest Bass directory.
