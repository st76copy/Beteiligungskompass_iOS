Participationcompass iOS -- A fully featured App for the Open Source Participationcompass web portal
========================================================================================================

## DESCRIPTION

Originally, the web platform "Beteiligungskompass.org" was initiated by the Bertelsmann Stiftung as a portal to help people in the public, private and not-for-profit sectors who need to involve a wider group of people in their work. The portal was created to provide information, advice, case studies and opportunities to share experiences with others helping to make public participation activities as effective as possible.

The portal is mainly aimed at people who are directly involved in planning, running or commissioning participation activities.

This is the Open Source release for the iOS App that interacts with the portal's database and lets users browse through the platform's catalogue for offline use. The App is a universal app and can be used on iPhone and iPad.

## SYSTEM REQUIREMENTS

* [Xcode 4.6.x](http://developer.apple.com)
* [OS X 10.8 Mountain Lion](https://itunes.apple.com/de/app/os-x-mountain-lion/id537386512?mt=12)

## DEVICE-COMPATIBILITY

* iOS Version 5.0

## INSTALLATION/SETUP

### 1. Prerequisites

1. Open Xcode
2. File --> Open --> beteiligungskompass.xcodeproj

### 2. Settings

You will find all settings in the following files:

* `../Supporting Files/Endpoints.h`

You will need the following parameters:

* `base_url`: This is the URL where your web portal is running.
* `base_url_without_http`: this is the plain hostname which is used for storing passwords
* `API_KEY`: This key is needed to interface with the Web portal's API.

### 3. Generating the default Database

**VERY IMPORTANT:**

Unlike the Android app, the iOS app converts the database. Therefore to generate the default database you have to run the app in the simulator and perform a sync. Copy the database file off the Simulator's app directory (~/Library/Application Support/iPhone Simulator/...)

### 4. Generating Assets

Updating the base assets is the same: simply zip the thumbnails folder from within the iPhone Simulator and add it to the project.

## FOLDER STRUCTURE

	PROJECTFOLDER
    .
    ├── Beteiligungskompass
    │   ├── Comm
    │   ├── JSON
    │   ├── Local Data
    │   ├── Supporting Files
    │   │   ├── App Icons and Default Screen
    │   ├── View Controllers
    │   │   ├── About
    │   │   ├── Add Nodes
    │   │   │   ├── Study
    │   │   │   ├── event
    │   │   │   ├── expert
    │   │   │   ├── method
    │   │   │   ├── news
    │   │   │   └── qa
    │   │   ├── ArticleDetails
    │   │   │   ├── image view
    │   │   │   └── subclasses
    │   │   ├── ArticleList
    │   │   │   └── Cell Templates
    │   │   ├── Dashboard
    │   │   ├── Favorites
    │   │   │   └── Cell Templates
    │   │   ├── Filter
    │   │   │   └── Filter Selection
    │   │   ├── Import
    │   │   │   └── minizip
    │   │   ├── InfoContact
    │   │   ├── Login
    │   │   ├── Planner
    │   │   │   └── Container
    │   │   ├── SlideIn ViewController
    │   │   ├── Video Block
    │   │   └── sharing
    │   ├── Views
    │   ├── de.lproj
    │   ├── en.lproj
    │   └── gfx
    ├── Beteiligungskompass.xcodeproj




* **`/Supporting Files`**: The assets folder contains the initialize data for the first App install without any syncs, alongside with iOS-typical files

**IMPORTANT:** DON'T CHANGE THE NAMES OF THESE FILES!

* **`/Supporting Files/thumb.zip`**: Includes the images and videos from all articles.

* **`/View Controllers`**: contains all view controllers

* **`/Views`**: contains a set of base views used throughout the project

* **`/Comm`**: contains all communication-relevant classes

* **`/Local Data`**: contains the entity classes generated by core data