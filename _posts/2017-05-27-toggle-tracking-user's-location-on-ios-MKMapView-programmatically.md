---
layout: post
title: 'Toggle tracking user''s location on iOS MKMapView programmatically'
categories: Cocoa/iOS
tags: [iOS, swift]
---
<!--more-->
# 1. Import MapKit framework from Project setting.



# 2. Initialize MKMapView and set it as main view for the ViewController.

<img src="https://cloud.githubusercontent.com/assets/12888144/26548160/acedd0d2-44ad-11e7-89d9-5b19e9bb079f.gif" class="img-responsive">

{% gist hskang9/fb5bf515bb856200ab5574e0603e1963 %}


# 3. Import CoreLocation and build locationManager for tracking the user's location

{% gist hskang9/72bfe1738b4a5af5f27bc284855ad893 %}

# 4. Make button programmatically and add programmatic control with event

{% gist hskang9/fa847092478b528c1baa3ba81c0470c2 %}

