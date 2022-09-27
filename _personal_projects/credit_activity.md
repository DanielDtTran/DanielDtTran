---
title: "Credit Activity Tracker"
excerpt: "Application for tracking monthly credit card usage."
number: 2
header:
    image: /images/personal_projects/credit_activity/header.png
    teaser: /images/personal_projects/credit_activity/teaser.png
toc: true
toc_sticky: true


gallery_features_1:
  - image_path: /images/personal_projects/credit_activity/years-2022-gallery.png
    url: /images/personal_projects/credit_activity/years-2022.png
    title: An example of the application tracking activity for 2022.
  - image_path: /images/personal_projects/credit_activity/years-2021-gallery.png
    url: /images/personal_projects/credit_activity/years-2021.png
    title: An example of the application tracking activity for 2021.
  - image_path: /images/personal_projects/credit_activity/years-2020-gallery.png
    url: /images/personal_projects/credit_activity/years-2020.png
    title: An example of the application tracking activity for 2020.

gallery_features_2:
  - image_path: /images/personal_projects/credit_activity/inactive-warning-gallery.png
    url: /images/personal_projects/credit_activity/inactive-warning.png
    title: Inactive cards are highlighted in yellow.
  - image_path: /images/personal_projects/credit_activity/inactive-danger-gallery.png
    url: /images/personal_projects/credit_activity/inactive-danger.png
    title: Extremely inactive cards are highlighted in red.    

gallery_features_3:
  - image_path: /images/personal_projects/credit_activity/sync-before-gallery.png
    url: /images/personal_projects/credit_activity/sync-before.png
    title: An example of navigating to the Sync Menu for syncing with YNAB.
  - image_path: /images/personal_projects/credit_activity/sync-menu.png
    url: /images/personal_projects/credit_activity/sync-menu.png
    title: Options found under the Sync Menu.
  - image_path: /images/personal_projects/credit_activity/sync-after-gallery.png
    url: /images/personal_projects/credit_activity/sync-after.png
    title: Tracking data is updated aftering syncing with YNAB.


---

## Project Description
Implements an application for tracking my personal credit card activity over multiple years.

The project also integrates with the API of You Need A Budget (YNAB), a service for budgeting
one’s finances. 

As a result, the application allows for quick and easy syncing with my personal YNAB account.
<br><br>


## Features
{% include gallery id="gallery_features_1" layout="third" caption="Supports tracking activity over multiple years." %}
{% include gallery id="gallery_features_2" layout="half" caption="Warns the user of inactive credit cards." %}
{% include gallery id="gallery_features_3" layout="third" caption="Integrates with YNAB for quick and easy tracking." %}
[Read PDF for even more features.](/documents/Python Projects.pdf){:target="_blank"}
<br><br>


## Motivation
Often, as one increasingly opens new credit cards with better reward structures, older and less
rewarding cards lose their appeal. Naturally, in this case, most would prefer to shift focus to their newer
cards. 

However, as the older cards are used less and less, or perhaps forgotten altogether, these cards
may face account inactivity. If the period of inactivity extends long enough, then the financial institution
may close the account.

I had first conceived of a tracking solution employing Excel to help prevent account closures.
However, the initial solution was written using Visual Basic for Applications (VBA) which introduced
difficulty when I aspired to make improvements. Furthermore, while Excel can be extremely intuitive
due to its ubiquity, the application is quite inefficient and slow compared to a specialized solution.
<br><br>


## Design Goals
* Remove the dependence on Excel and VBA by porting the initial solution to Python.
* Retain and adapt useful features of Excel, namely its grid of cells.
* Maximize the longevity of the solution by minimizing the number of Python dependencies.
* Improve the solution’s speed and footprint.
<br><br>


## Benefits
* Provides a lightweight application for tracking credit card usage.
* Integrates with my personal YNAB account, allowing for an effortless sync with the financial service.
* Ensures a long-term solution by minimizing Python dependencies, with the most likely point of
  failure being the `ynab-client` module.
<br><br>


## Notable Milestones & Roadblocks
{% include figure image_path="/images/personal_projects/credit_activity/progression.png" %}


## Dependencies
### Languages
<div class="notice">
<ul>
<li> Python 3.6 </li>
</ul>
</div>

### Python
<div class="notice--success">
<ul>
<li> pyqt5 </li>
<li> ynab-client </li>
</ul>
</div>