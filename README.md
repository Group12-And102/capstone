Event Search (Ticketmaster) Project Design
===

# Event Search

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
The app is a one-stop-shop allowing users to explore happening events around them which can be filtered based on their location and category. Users can mark favorites, get venue seat map and other relevant details.

### App Evaluation
- **Category:** Entertainment
- **Mobile:** This app would be developed for iOS devices
- **Story:** Allows user to type in keywords that may interest them. Then users are given a list of events based on the keywords and users are allowed to tap in to the event to find more information about it.
- **Market:** This app is open to any indivdual who would like to know more information about certain events
- **Habit:** This app could be used if individuals are interested in attending future events near them or some other places.
- **Scope:** This app will start with providing information about events such as date and time, location, artist, etc. Then maybe we could advance to allowing users to buy and resell tickets and event planning similar to ticketmaster application.

## Product Spec

### 1. User Stories (Required and Optional)


**Required Must-have Stories**

* Form to search events -- with submit and clear buttons.
* Table showing results from API call to get events
* Tap on table row to segue for that event's details
* Have 3 tabs on event details screen to switch between generic event details, artist details and venue details.

**Optional Nice-to-have Stories**

* Add a favorite button to event details, and show all favorite marked events on a separate screen
* Swipe left to delete marked favorite event (instead of a tapped button)

### 2. Screen Archetypes


   * Landing page (containing search form and results in a table)
   * Event Details screen when an event row is tapped
   * Favorites screen to show marked favorite events


### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Switch options between event details, artist/team details and venue details once the second screen (after an event row is tapped)


**Flow Navigation** (Screen to Screen)

* Tap on row in event search results to get to second screen
* Tap on favorites button to see list of marked favorite events

## Wireframes
<img src="https://imgur.com/aX1AiXI.jpg" width=800><br>


## Schema 
[This section will be completed in Unit 9]


### Models
Event Search Result: List/Array where each item contains [{eventId, eventDate, eventTime eventName, eventVenue, eventImage, eventCategory}]

Event Details: date, time name, ticketPrice, genre, venueName, seatMap, category

Venue Details: name, phoneNumber, openHours, address, childRule


### Networking
- Make API call to TicketMaster when search button of form is tapped.
- Sample API call results:
    - Event Search Results - https://shubham-jain-events-webapp.wl.r.appspot.com/getEvents?keyword=Pink&distance=10&category=&location=Detroit
    - Event Details - https://shubham-jain-events-webapp.wl.r.appspot.com/getEventDetails?eventId=k7vGF94XpYsjo
    - Venue Details - https://shubham-jain-events-webapp.wl.r.appspot.com/getVenueDetails?venueName=Comerica%20Park
