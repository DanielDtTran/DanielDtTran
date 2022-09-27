---
title: "Blu-ray Release Tracker"
excerpt: "Automatic searching and notifying of desired Blu-ray releases."
number: 3
header:
    image: /images/personal_projects/bluray_tracker/header.png
    teaser: /images/personal_projects/bluray_tracker/teaser.png
toc: true
toc_sticky: true


gallery_features_catalog:
  - image_path: /images/personal_projects/bluray_tracker/catalog-new-gallery.png
    url: /images/personal_projects/bluray_tracker/catalog-new.png
    title: The project continously retrieves upcoming movies and presents them to the user within a catalog.
  - image_path: /images/personal_projects/bluray_tracker/catalog-tracking-gallery.png
    url: /images/personal_projects/bluray_tracker/catalog-tracking.png
    title: Media with desired Blu-ray releases are stored in a separate catalog.

gallery_features_inspect:
  - image_path: /images/personal_projects/bluray_tracker/inspect-gui-gallery.png
    url: /images/personal_projects/bluray_tracker/inspect-gui.png
    title: Clicking on a media reveals its details and tracking options.
  - image_path: /images/personal_projects/bluray_tracker/inspect-focus.png
    url: /images/personal_projects/bluray_tracker/inspect-focus.png
    title: Inspecting the media after choosing to track its 1080p Blu-ray.

gallery_features_search:
  - image_path: /images/personal_projects/bluray_tracker/search-dialog-gallery.png
    url: /images/personal_projects/bluray_tracker/search-dialog.png
    title: Specific media can be searched for and then tracked.
  - image_path: /images/personal_projects/bluray_tracker/search-pending-gallery.png
    url: /images/personal_projects/bluray_tracker/search-pending.png
    title: Tracking the 1080p release of <i>Eternals</i>.
  - image_path: /images/personal_projects/bluray_tracker/search-found-gallery.png
    url: /images/personal_projects/bluray_tracker/search-found.png
    title: Found Blu-ray releases are automatically pushed to my smartphone.


---

## Project Description
Project for tracking the Blu-ray releases of desired media.

The project consists of multiple components:
1. GUI Application
2. Raspberry Pi 3 / 4
3. Smartphone

The GUI application facilitates selecting desired media for tracking. Next, the Raspberry Pi is a low-
power and low-cost solution for storing all data employed by the application within a database;
moreover, the Raspberry Pi can perpetually check for Blu-ray releases at set intervals of time. Finally,
once a release has been found, then the Raspberry Pi will send a push notification to my smartphone.
<br><br>


## Features
{% include gallery id="gallery_features_catalog" layout="half" caption="Desired Blu-rays are selected from a catalog of upcoming movies." %}
{% include gallery id="gallery_features_inspect" layout="half" caption="Media can be clicked on for a closer look with more details." %}
{% include gallery id="gallery_features_search" layout="third" caption="Supports searching and tracking for specific media." %}
[Read PDF for even more features.](/documents/Python Projects.pdf){:target="_blank"}
<br><br>


## Motivation
I enjoy watching movies; however, not all movies deserve the same level of interest: for some movies, I
would prefer watching at home rather than in the cinema. Ironically, I find difficulty in staying informed
of the Blu-ray release of these movies.

In a similar manner, for TV shows, often I would prefer the greater bandwidth (quality) offered via Blu-
ray as compared to streaming services.

Therefore, I aspired to design a solution to inform me of upcoming media and minimize as much effort
required from me to track their Blu-ray releases.
<br><br>


## Design Goals
* Provide a continually updating catalog of upcoming movies, reducing the need for me to stay updated with current releases.
* Streamline the user experience by reducing or hiding loading times as much as possible.
* Utilize the Raspberry Pi as a server for storing media data and tracking releases 24/7.
<br><br>


## Benefits
* Eliminates the need to manually check for Blu-ray releases.
* Automatically notifies me of desired releases.
<br><br>


## Notable Milestones & Roadblocks
{% include figure image_path="/images/personal_projects/bluray_tracker/progression.png" %}


## Dependencies
### Languages
<div class="notice">
<ul>
<li> Python 3.8 </li>
</ul>
</div>

### Python
<div class="notice--success">
<ul>
<li> requests </li>
<li> bs4 </li>
<li> pyqt5 </li>
<li> omdb </li>
<li> cinemagoer </li>
<li> python-dateutil </li>
<li> pushbullet.py </li>
<li> mysql-connector-python </li>
</ul>
</div>

### External
<div class="notice--info">
<ul>
<li> Smartphone </li>
<li> Raspberry Pi 3 or 4 </li>
<li> MariaDB </li>
<li> HeidiSQL </li>
</ul>
</div>