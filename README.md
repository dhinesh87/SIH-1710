# Smart India Hackathon Workshop
# Date:26.10.26
## Register Number:212223040040
## Name: Dhinesh M
## Problem Title
SIH 1710: Enhancing Navigation for Railway Station Facilities and Locations
## Problem Description
Background: Railway stations are complex environments with numerous facilities and locations such as ticket counters, platforms, restrooms, food courts, and waiting areas. Passengers often face difficulties in navigating these spaces, especially in large or unfamiliar stations. Efficient and user-friendly navigation systems are crucial for improving passenger experience, reducing congestion, and ensuring timely travel connections. Description: The problem involves developing a comprehensive navigation solution for railway stations that assists passengers in locating various facilities and destinations within the station premises. This includes creating detailed maps, providing real-time directions, and integrating features such as accessibility options for individuals with disabilities. The solution should be intuitive, easy to use, and accessible via multiple platforms, including mobile devices and digital kiosks. Key challenges include updating navigation information in real-time, ensuring accuracy, and accommodating the diverse needs of all passengers. Expected Solution: The expected solution is a multi-platform navigation system that provides detailed, real-time directions to all facilities and locations within a railway station. This system should include: A mobile application with 3D interactive maps and step-by-step navigation. Digital kiosks located throughout the station with touch-screen interfaces. Voice-guided navigation for visually impaired passengers. Regular updates to reflect changes in station layout and facility locations. Integration with existing railway apps and services for seamless user experience. The solution should enhance the overall passenger experience by reducing confusion, saving time, and improving accessibility within the station.

## Problem Creater's Organization
Ministry of Railway

## Idea
SmartRail Navigator – AI-Powered Railway Station Navigation System

SmartRail Navigator is a smart navigation system that helps passengers find platforms, ticket counters, restrooms, food courts, waiting halls, exits, and other facilities inside railway stations.

It uses interactive 2D/3D maps, GPS where available, indoor positioning, voice guidance, and accessible navigation features to guide passengers to their destinations efficiently.

## Proposed Solution / Architecture Diagram

Proposed Solution

Our solution is a mobile and web-based application that provides real-time indoor navigation inside railway stations.

Key Features:

Interactive Station Map: Displays platforms, entrances, exits, lifts, stairs, ticket counters, and other facilities.
Smart Route Planning: Finds suitable routes from the passenger's current location to the selected destination.
Voice Navigation: Provides step-by-step voice instructions for passengers, including visually impaired users.
Accessibility Mode: Suggests wheelchair-friendly routes using ramps and lifts.
Live Train Information: Displays train schedules, platform information, and delay updates when reliable railway data is available.
Multilingual Support: Supports English, Tamil, Hindi, and other languages.
Digital Kiosk Support: Provides touch-screen navigation at important locations inside railway stations.
Emergency Navigation: Helps users locate emergency exits, first-aid facilities, and help desks.
Architecture Diagram
      
```


        PASSENGERS
             |
             v
    CLIENT APPLICATIONS
   (Mobile App / Web App / Kiosk)
             |
             v
       BACKEND SERVER
       (Python + FastAPI)
             |
     +-------+--------+
     |       |        |
     v       v        v
  Station  Navigation Database
    Map     Engine  (PostgreSQL)
     |       |
     |       v
     |   Route Calculation
     |   (Dijkstra / A*)
     |       |
     +-------+
             |
             v
    INDOOR LOCATION DETECTION
       (QR Codes / BLE)
             |
             v
      VOICE NAVIGATION
      (Text-to-Speech)
             |
             v
       FINAL OUTPUT
 (Shortest Route, Facility Location,
  Accessibility & Train Information)
```



Technologies used in the architecture: React, Python, FastAPI, PostgreSQL, OpenStreetMap, and a graph-based route-finding algorithm.

Note: GPS alone may not provide accurate indoor positioning. The system can initially use manually selected locations, QR codes, or mapped checkpoints. Bluetooth beacons or other indoor-positioning technologies can be added later.


## Use Cases


1	Platform Navigation	Guides passengers from the station entrance to their required platform.
2	Facility Locator	Helps users locate restrooms, food courts, ticket counters, and waiting halls.
3	Accessible Navigation	Finds routes suitable for wheelchair users and passengers with mobility difficulties.
4	Voice Assistance	Provides audio directions for visually impaired passengers.
5	Train Information	Displays train timings and platform details using available railway data.
6	Emergency Assistance	Helps passengers locate exits, first-aid rooms, and help desks.
7	Multilingual Navigation	Provides instructions in the passenger's preferred language.
8	Digital Kiosk Navigation	Allows passengers to search for destinations using a station kiosk.


## Technology Stack

The SmartRail Navigator project uses React.js and Tailwind CSS for frontend development, React Native with Expo for mobile application development, and Python with FastAPI for backend development. PostgreSQL is used for storing railway station locations, facilities, and route information. OpenStreetMap and React Leaflet are used to display interactive maps, while Dijkstra’s Algorithm or A* Algorithm is used to calculate the shortest and most suitable routes. QR codes are used for indoor location identification, and Text-to-Speech technology provides voice-guided navigation for visually impaired passengers. Git and GitHub are used for version control, while Vercel and Render can be used for deploying the frontend and backend applications.

## Dependencies
The following resources and dependencies are required to develop the project.

A. Software Dependencies

Frontend

Node.js and npm
React.js
Tailwind CSS
React Leaflet, if using Leaflet maps

Backend

Python 3.11 or a compatible version
FastAPI
Uvicorn
SQLAlchemy
Pydantic

Database

PostgreSQL
PostGIS, if advanced spatial queries are needed

Mobile Application

React Native
Expo
QR-code scanning library
B. Data Dependencies
Railway station floor plans or mapped station layouts.
Locations of platforms, entrances, exits, and facilities.
Connections between corridors, stairs, lifts, and platforms.
Accessibility information about ramps, lifts, and wheelchair-friendly routes.
Train schedules and platform information from authorized or reliable data sources.
Updated information about temporarily closed facilities and route restrictions.
C. Hardware Dependencies
Smartphone or computer for development and testing.
Android phone for mobile application testing.
Digital kiosk or touchscreen for kiosk testing.
QR-code markers for identifying mapped locations.
Optional Bluetooth Low Energy (BLE) beacons for more advanced indoor positioning.

Important: Actual railway station maps and live railway data may require permission or an official data source. Begin with a small, manually mapped station prototype before attempting integration with live railway systems.
