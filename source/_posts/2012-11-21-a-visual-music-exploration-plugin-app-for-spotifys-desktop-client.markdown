---
layout: post
title: "A Visual Music Exploration Plugin App for Spotify's Desktop Client"
date: 2012-11-21 20:21
comments: true
categories: App Research
---


This project which I've finished recently is in its essence implementing an innovative way of visualizing Spotify music collection data. It's mainly geared towards discovery of similar music related to the currently played tracks of a user. Technically, the project partially builds upon the foundation layed out with a previous labs project -- here's a [report](http://sftb.herokuapp.com/docs/report.pdf) (PDF). Organisationally, it was done as a cooperation with [Spectralmind](http://www.spectralmind.com/) and the [MIR group](http://ifs.tuwien.ac.at/mir/) of Vienna University of Technology.


## Implementation

Basically, the app connects to **Last.fm** data for similarity computation with their (more or less) RESTful web service API via JSONP. In addition to that, **Spotify**'s desktop client [plugin apps](https://developer.spotify.com/technologies/apps/) JS API is used pretty heavily. The graphics are rendered as interactive SVG through **Raphaël.js**. Plus, **Backbone.js** is applied as a mean to improve structure and, consequently, maintainability of the app. For layouting the animated visualization itself a force-based [spring graph](http://en.wikipedia.org/wiki/Force-based_algorithms_%28graph_drawing%29) algorithm implementation is employed which was orginally written within Google's Caja project and now adapted for the specific use case here.


## Functionality

In the beginning, the user sees the current track symbolized by a central blue bubble and a loading spinner indicating app activity. Here's a screenshot:

{% img /images/spotify-sonarflow/screenshot1.png 'Screenshot 1' 'Screenshot 1' %}

After that, found similar tracks are arranged as red bubbles in a concentric circle around the central one. Again, a screenshot:

{% img /images/spotify-sonarflow/screenshot2.png 'Screenshot 2' 'Screenshot 2' %}

Here's how the actual animated spring graph algorithmic layouting visualization initially looks like:

{% img /images/spotify-sonarflow/screenshot3.png 'Screenshot 3' 'Screenshot 3' %}

And this is how it can look like when the animation finished rendering:

{% img /images/spotify-sonarflow/screenshot4.png 'Screenshot 4' 'Screenshot 4' %}

The history of played tracks is visualized as a diagonal, interactive sort of a time axis which can also be seen here:

{% img /images/spotify-sonarflow/screenshot5.png 'Screenshot 5' 'Screenshot 5' %}

Intuitively, clicking a bubble plays the respective track in the Spotify audio player, BTW.


## Conclusion

The approach proved to be viable and it can be indeed worthwhile searching and discovering new music fitting to one's individual taste in an entertaining way with this Spotify plugin app. Nevertheless, there are still numerous details where improvements and enhancements are possible. E.g., the graphics and visualization could be made more pleasant. Apart from that, also further tweaking related to similarity computation could be done. Yet, as a research prototype demonstrating a proof of concept this is sufficient, it was fun building it, and possibly it'll show up within a polished product in one way or another. :)
