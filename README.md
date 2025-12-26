# PWS Multi-Station Viewer

A single-page HTML/JavaScript app for **comparing measurements from multiple personal weather stations (PWS)** that report to Weather Underground / the Weather Company API.

**In order to use this you must have your own Weather Underground API key**

The main idea: you can pick several stations around you (or anywhere), and see how their temperature, humidity, pressure, wind, etc. compare over the same time range.

---

## Features

- 🌍 **Interactive map (Leaflet + OpenStreetMap)**
  - Pan and zoom to any location.
  - Search for nearby PWS using the Weather.com PWS API.
  - Click a station marker to add/remove it from your comparison list.

- 📋 **Station selection panel**
  - Shows the list of currently selected stations.
  - Displays station ID and coordinates.
  - Quick “Remove” button for each station.

- 📈 **Time-series chart (Plotly)**
  - Plots historic data from all selected stations on a single chart.
  - Measurement selector:
    - Temperature
    - Dew point
    - Humidity
    - Pressure
    - Wind speed
    - Wind gust
    - Precipitation rate
    - Precipitation total
  - Time range selector:
    - Past 24 hours
    - Past week
    - Past month
    - Custom (pick specific start/end date-time)
  - Legend includes both **station name and station ID** so you can tell which trace is which.

- 🖥️ **Flexible layout & fullscreen**
  - Top half: map (left 75%) + station list (right 25%)
  - Bottom half: chart
  - Fullscreen buttons for:
    - Map only
    - Chart only

- 🔑 **API key persistence**
  - Uses `localStorage` to remember **your** Weather.com API key in your browser.
  - Other users must enter their own key the first time they use the app.

---

## Why this app?

Weather Underground and the Weather Company APIs expose a huge network of personal weather stations—but it’s not easy to:

- Compare **multiple** nearby stations on one plot.
- Visually sanity check readings (e.g., see if your station is running “hot” vs neighbors).
- Look at trends over a chosen time window across several stations.

This app is meant to solve exactly that:

> **“Let me put several local PWS on a map, select them, and see their plots on the same graph so I can compare their measurements over time.”**

It’s useful for:

- Checking calibration / bias of your own station.
- Comparing microclimates in a neighborhood or region.
- Spotting obviously bad sensors by eye.
- Just geeking out over local weather variations.


