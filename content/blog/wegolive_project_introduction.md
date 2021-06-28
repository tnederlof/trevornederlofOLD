---
title: "WeGoLive Full Stack Web Application Overview"
date: 2021-06-28T09:40:25-04:00
draft: false
---


# Introduction

Welcome to the first post of my first blog! My name is [Trevor Nederlof](https://www.trevornederlof.me/about/), and I am passionate about open-source software, web development, and geospatial analysis. With many fantastic software pieces out there, it can be hard to figure out how they all fit together. For this reason, I wanted to build a modern full-stack web application involving a whole bunch of open-source technologies and explain each step. I sincerely hope this inspires others to blog, teaches the basics of some neat technology, and spawns collaboration.

I would love to hear feedback on this post and future posts. Why did you read the post? What pieces of this stack interest you the most? Suggestions on changes? Questions? Do not be shy! Please find me on Twitter at [@tnederlof](https://twitter.com/tnederlof).

This post and the ones that follow will document the creation of WeGoLive; lets get started!


# Overview

WeGoLive is a web application that will solve the following hypothetical issue (although I hope you can see real-world use cases for various parts of this application)...

The citizens of Nashville are unhappy with the delivery and visualization of their real-time bus data from the WeGo operator. Grace waited 25 minutes at her local bus stop just yesterday due to a delayed bus in traffic. She tried her phone, but the ancient transit agency website barely loaded on her phone, and even once the page loaded, the map was unreadable on her tiny screen. Wouldn't it be great to have a real-time map of the buses in Nashville where users could add comments to the trips to crowdsource additional information (such as the friendliest driver, super packed, etc.)?

WeGoLive will solve Grace's problem using a combination of technologies outlined at the end of this post and meet these high-level objectives:
1. Show real-time bus information for Nashville on an easy to read interactive web map
2. Allow users to search a location, get a list of the closest bus stops, and show the time until the next bus arrives
3. Allow users to leave real-time feedback (crowdsourced information)  

# Technology Stack

The overall framework we will use is [Phoenix](https://phoenixframework.org/), written in [Elixir](https://elixir-lang.org/). Other popular choices include [Django](https://www.djangoproject.com/) written in [Python](https://www.python.org/) and [Ruby on Rails](https://rubyonrails.org/) written in [Ruby](https://www.ruby-lang.org/en/). Many tutorials have been written using Django and Ruby on Rails; this is not a post to say they are bad frameworks, I just believe Phoenix is better suited due to its speed, handling of real-time data, syncing across clients, and interop with javascript via [liveview](https://hexdocs.pm/phoenix_live_view/Phoenix.LiveView.html).


## Frontend
Phoenix has a templating system which we will use along with [tailwindcss](https://tailwindcss.com/) to style the frontend. For the client-side interactivity parts of the app, we will use plain Javascript and interact with the JS code from the server/backend side using [liveview](https://hexdocs.pm/phoenix_live_view/Phoenix.LiveView.html). [OpenLayers](https://openlayers.org/) will be used to create a multi-layered interactive web map.  


## Backend
Our database will be [PostgreSQL](https://www.postgresql.org/) which Phoenix interacts with via [Ecto](https://hexdocs.pm/ecto/Ecto.html), an incredibly well-designed ORM. The database will hold user account information and feedback. We will use the [PostGIS](https://postgis.net/) extension for PostgreSQL to store and analyze geospatial data such as bus routes, stops, and trips.

We will use the [GTFS Realtime data exchange](https://developers.google.com/transit/gtfs-realtime) to retrieve real-time bus trip data in a [protocol buffer format](https://developers.google.com/protocol-buffers). While GTFS is specific to transit data, protocol buffers (or protobufs for short) have increased in popularity with a wide variety of applications.

To generate interactive maps, we will use [OpenMapTiles](https://openmaptiles.org/) to create [OpenStreetMap](https://www.openstreetmap.org/) based set of vector tiles, which OpenLayers can then display. To allow users to search locations, we will interact with the [OpenCage Geocoding API](https://opencagedata.com/), which has a generous free tier and uses open data to power it.

Lastly, we will use [PubSub](https://hexdocs.pm/phoenix_pubsub/Phoenix.PubSub.html), a powerful feature built into Phoenix to keep all of the users viewing the application in sync so when one provides feedback, everyone sees it in real-time.  

# What Next?

This project will take some time to come together due to the moving parts, but I think you will be impressed by how much we can achieve building intelligently on the shoulders of these giant technologies. I will try to post at least once a week over the next couple of months until WeGoLive is alive. Check back soon or follow [me on twitter](https://twitter.com/tnederlof) to find new posts as the app progresses.