week 15 Homework
Unit 15 Homework: Visualizing Data with Leaflet
Background
USGS

The United States Geological Survey, or USGS for short, is responsible for providing scientific data about natural hazards, the health of our ecosystems and environment, and the impacts of climate and land-use change. Their scientists develop new methods and tools to supply timely, relevant, and useful information about the Earth and its processes. As a new hire, you will be helping them out with an exciting new project!

The USGS is interested in building a new set of tools that will allow them to visualize their earthquake data. They collect a massive amount of data from all over the world each day, but they lack a meaningful way of displaying it. Their hope is that being able to visualize their data will allow them to better educate the public and other government organizations (and hopefully secure more funding) on issues facing our planet.

Before You Begin
Create a new repository for this project called leaflet-challenge. Do not add this homework to an existing repository.

Clone the new repository to your computer.

Inside your local git repository, create a directory for the Leaflet challenge. Use the folder names to correspond to the challenges: Leaflet-Part-1 and Leaflet-Part-2.

This homework uses both HTML and JavaScript, so be sure to add all the necessary files. These will be the main files to run for analysis.

Push the above changes to GitHub.

Instructions


The instructions for this activity are broken into two parts:

Part 1: Create the Earthquake Visualization

Part 2: Gather and Plot More Data (Optional)

Part 1: Create the Earthquake Visualization
2-BasicMap

Your first task is to visualize an earthquake dataset. Complete the following steps:

Get your dataset. To do so, follow these steps:

The USGS provides earthquake data in a number of different formats, updated every five minutes. Visit the USGS GeoJSON Feed page and choose a dataset to visualize. The following image is an example screenshot of what appears when you visit this link:
3-Data

When you click a dataset (such as "All Earthquakes from the Past 7 Days"), you will be given a JSON representation of that data. Use the URL of this JSON to pull in the data for the visualization. The following image is a sampling of earthquake data in JSON format:
4-JSON

Import and visualize the data by doing the following:

Using Leaflet, create a map that plots all the earthquakes from your dataset based on their longitude and latitude.

Your data markers should reflect the magnitude of the earthquake by their size and the depth of the earthquake by color. Earthquakes with higher magnitudes should appear larger, and earthquakes with greater depth should appear darker in color.

Hint: The depth of the earth can be found as the third coordinate for each earthquake.

Include popups that provide additional information about the earthquake when its associated marker is clicked.

Create a legend that will provide context for your map data.
This repo works through the requirements of the homework and completes some of the bonus activities.

The JS file creates several layers initially, in order for users to have access to a street map or a (more useful in my opinion) topographic map. The default view centres on Africa to get the best overview.

The code then renders the key to the colour system, using a defined function for consistency.

It take the GeoJson data through D3 and loops through the list of earthquakes inside the response. For each earthquake, a circle is generated from latititude, longitude, depth, and magnitude.
