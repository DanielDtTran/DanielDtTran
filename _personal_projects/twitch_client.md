---
title: "Custom Twitch.tv Client"
excerpt: "Custom client for watching multiple livestreams from Twitch.tv simultaneously."
number: 1
header:
    image: /images/personal_projects/twitch_client/header.png
    teaser: /images/personal_projects/twitch_client/teaser.png
toc: true
toc_sticky: true


gallery_features_1:
  - image_path: /images/personal_projects/twitch_client/features-single-gallery.png
    url: /images/personal_projects/twitch_client/features-single.png
    title: "An instance of the client in viewing one livestream with its corresponding chatroom."
  - image_path: /images/personal_projects/twitch_client/features-dual-gallery.png
    url: /images/personal_projects/twitch_client/features-dual.png
    title: "An instance of the client in viewing two livestreams with their corresponding chatrooms."
  - image_path: /images/personal_projects/twitch_client/features-quad-gallery.png
    url: /images/personal_projects/twitch_client/features-quad.png
    title: "An instance of the client in viewing four livestreams."

gallery_features_2:
  - image_path: /images/personal_projects/twitch_client/features-multi-gallery.png
    url: /images/personal_projects/twitch_client/features-multi.jpg
    title: "Three clients viewing 4 livestreams across 3 monitors."


---

## Project Description
Implements a customized client for viewing livestreams from Twitch.tv.

An instance of the client supports simultaneously viewing up to 4 livestreams
with 3 viewing settings:

1. a single stream with its chatroom
2. two streams with their respective chatrooms
3. four streams

Futhermore, the project supports viewing multiple instances of a client over
multiple monitors (up to 3). Therefore, **a maximum of 12 livestreams** can
be viewed simultaneously.
<br><br>


## Features
{% include gallery id="gallery_features_1" layout="third" caption="Supports up to 4 livestreams simultaneously." %}
{% include gallery id="gallery_features_2" layout="" caption="Multiple clients can be launched for multi-monitor support." %}
[Read PDF for even more features.](/documents/Python Projects.pdf){:target="_blank"}
<br><br>


## Motivation
At the initial time of project conception, Twitch.tv did not offer a method to view multiple livestreams
simultaneously.

Thus, one would have to commonly choose one of the following compromises:

1. Open multiple browser tabs but only focus on one, potentially missing entertaining segments of
   the other livestreams.
2. Open multiple browser tabs and manually organize the windows but also having to endure the
   tedium, especially as the number of livestreams scale.
3. Open only one browser tab but forgo all other livestreams, completely unaware of any
   entertaining segments of the other livestreams.

In this regard, I conceived of the idea of a customized client, capable of viewing multiple livestreams
simultaneously and being controlled effortlessly through hotkeys.
<br><br>


## Design Goals
* The client must be capable of viewing multiple livestreams simultaneously.
* Hotkeys should be implemented to facilitate quick control of the client.
<br><br>


## Benefits
* Circumvents ads from Twitch.tv by leveraging the `streamlink` module
* Integrates with my personal Twitch.tv account
* Minimizes footprint, compared to a web browser, by embedding the mpv media player into the Qt
  GUI
* Provides quick control via hotkeys, removing the need to resize or move the client by dragging
* Allows for the alerting of livestreams under special conditions, such as when viewer count hits a
  desired threshold, usually indicating that a special event is occurring
<br><br>


## Notable Milestones & Roadblocks
{% include figure image_path="/images/personal_projects/twitch_client/progression.png" %}


## Dependencies
### Languages
<div class="notice">
<ul>
<li> Python 3.8 </li>
<li> AutoHotkey 1.1 </li>
</ul>
</div>

### Python
<div class="notice--success">
<ul>
<li> requests </li>
<li> streamlink </li>
<li> psutil </li>
<li> pyqt6 </li>
<li> python-mpv </li>
<li> python-twitch-client </li>
</ul>
</div>

### External
<div class="notice--info">
<ul>
<li> Libmpv </li>
<li> Chatterino 2 </li>
</ul>
</div>
