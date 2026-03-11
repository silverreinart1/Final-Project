# 🏍️ MotoRadar

MotoRadar is a platform that brings together essential features for motorcyclists into one application. The goal is to create an active and useful community where users can share routes, information, events, and request assistance while on the road if needed.

---

## 🚀 Project Goal

To create a system (API + user interface) that supports the motorcyclist community and makes the riding experience safer, more exciting, and improves the speed of information sharing.

---

## 🔗 Links

- 🎨 [Figma](https://www.figma.com/design/TGvAjL17XIaSoKemeAOeQO/FINAL_PROJECT?node-id=0-1&p=f&t=bNDEiI4frhEMroet-0)
- 📋 [Jira Board](https://silverreinart01-1760074771033.atlassian.net/jira/software/projects/SMS/boards/1)
- 🤳[Jira Confluence][https://silverreinart01-1760074771033.atlassian.net/wiki/x/AwAC](https://silverreinart01-1773125029243.atlassian.net/wiki/x/AQAH)

---

## 🛠️ Tech Stack for MotoRadar

| Layer       | Technology                                       | Notes                                                      |
| ----------- | ------------------------------------------------ | ---------------------------------------------------------- |
| Backend API | Firebase (Firestore + Realtime DB + Auth)       | Serverless backend, user authentication, route sharing, SOS alerts |
| Database    | sqflite                                          | SQLite plugin for Flutter, store GPS points and rides locally |
| Real-time   | Firebase Realtime Database + Cloud Messaging    | Live user map, SOS alerts, push notifications             |
| Frontend    | Flutter (Dart)                                  | Cross-platform mobile app, UI, map integration            |
| Maps        | Google Maps SDK for Flutter                      | Display routes, polylines, live users, markers           |
| Deployment  | Direct APK install / Firebase App Distribution  | Free testing on Android devices; optional Play Store deployment |

---

# MotoRadar – Motorcycle Route Tracker

MotoRadar is a **Flutter-based motorcycle tracking application** designed for riders who want to record their routes, share rides with the community, and get help in emergencies.

The app allows riders to:

* Track rides using GPS
* View ride statistics
* Share routes with other riders
* See nearby riders in real time
* Send SOS alerts when help is needed
* Use a community board for events, gear, and services

---

# System Architecture

MotoRadar follows a **client–server architecture**.

## Mobile Client (Flutter)

Responsible for:

* User interface
* GPS tracking
* Map rendering
* Ride statistics
* Local data storage

---

## Firebase Backend

Firebase provides:

* User authentication
* Shared ride storage
* Real-time location updates
* SOS alerts and notifications

---

## Local Storage (SQLite)

SQLite is used for:

* Storing rides locally
* Saving GPS coordinates
* Supporting offline tracking

---

# Core Features

## Route Tracking

* GPS-based route recording
* Displays **distance, time, and average speed**
* Routes displayed on **Google Maps with polylines**

---

## Route Sharing

Riders can share routes with the community.

Routes include:

* Title
* Description
* Difficulty level
* Road type (asphalt, offroad, mixed)
* Photos

---

## Emergency Assistance (SOS)

If a rider needs help:

* The rider can mark their **exact location**
* A **description of the issue** can be added (e.g., mechanical failure)
* **Nearby users receive notifications**

---

## Live User Map

* Displays **active riders on the map**
* Visibility can be **enabled or disabled**
* Riders can **join others on the same route**

---

## Info Board & Classifieds

A community board for:

* Motorcycle events
* Parts and bike sales
* Gear listings
* Workshop and repair services

Users can filter posts by:

* Topic
* Location
* Date

---

# Database Structure

## Firestore Collections

### users

```
users
 ├── id
 ├── username
 ├── avatar
 ├── visibility
 └── lastLocation
```

### routes

```
routes
 ├── id
 ├── userId
 ├── title
 ├── description
 ├── roadType
 ├── difficulty
 ├── polyline
 ├── rating
 └── createdAt
```

### posts

```
posts
 ├── id
 ├── category
 ├── title
 ├── description
 ├── imageUrl
 ├── location
 └── createdAt
```

---

# Local Database (SQLite)

### rides

```
rides
 ├── id
 ├── startTime
 ├── endTime
 ├── distance
 └── avgSpeed
```

### gps_points

```
gps_points
 ├── id
 ├── rideId
 ├── latitude
 ├── longitude
 └── timestamp
```

---

# User Flow

1. The user **registers or logs in** using Firebase Authentication.

2. The rider starts a ride using the **Start Ride** button.

3. **GPS coordinates are recorded locally** using SQLite.

4. The route is displayed on **Google Maps with a polyline**.

5. When the ride ends, the user can:

* Save the ride locally
* Share the ride online

6. Other users can:

* View shared routes
* Rate routes

7. If a rider needs help, they can trigger an **SOS alert**, sending their location to nearby riders.

---

# Project Structure (Flutter)

```
lib/
 ├── screens/
 ├── models/
 ├── services/
 ├── widgets/
 ├── database/
 └── main.dart
```

**screens** – app pages and UI
**models** – data models
**services** – Firebase and API logic
**widgets** – reusable UI components
**database** – SQLite implementation

---

# Development Roadmap

This roadmap outlines the development plan for MotoRadar.

---

## Phase 1 – Project Setup

* Install Flutter and Android Studio
* Initialize Flutter project
* Set up Firebase project
* Connect Firebase to the app
* Add required packages

**Deliverable**

Basic Flutter app running with Firebase connected.

---

## Phase 2 – Local Route Tracking

* Implement GPS tracking
* Create SQLite database
* Add **Start / Stop ride buttons**
* Calculate ride statistics
* Display route on map

**Deliverable**

Users can record rides and view route statistics.

---

## Phase 3 – Route Sharing

* Add Firestore integration
* Sync rides to cloud
* Add ride metadata
* Display shared routes

**Deliverable**

Users can view and share routes online.

---

## Phase 4 – Real-Time Features

* Live rider location
* Map showing nearby users
* SOS emergency alerts
* Push notifications

**Deliverable**

Live map and emergency alerts working in real time.

---

## Phase 5 – Info Board

* Firestore **posts** collection
* Categories (events, classifieds, services)
* Image uploads with Firebase Storage
* Filters by topic and location

**Deliverable**

Users can post and browse community information.

---

## Phase 6 – Testing and Improvements

* Improve UI and usability
* Test GPS accuracy
* Test real-time features
* Fix bugs and optimize code

**Deliverable**

Stable and functional application.

---

