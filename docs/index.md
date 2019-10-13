# Location Triggers
Location Triggers is part of Autocuts Suite, a collection of shortcuts that greatly enhance automation on iOS 13. It works with [Autocuts](https://adamtow.github.io/autocuts) to automatically run shortcuts in the background based on your location while you use your iOS device — no need to tap on a button in a notification!

![Location Triggers](https://adamtow.github.io/location-triggers/images/location-triggers-screens.png)

## What is Autocuts?
Autocuts is a background shortcut manager that works on top of Open App personal automation feature of Shortcuts in iOS 13. Choosing your most commonly used applications to launch Autocuts in the background ensures that your shortcuts are constantly working behind the scenes to do things like:

- Set Do Not Disturb for specific calendar events.
- Turning on Low Power Mode when your battery falls below a certain percentage.
- Sending text messages, emails, or web requests at certain times of the day or when you arrive or leave locations.

## Download
You can get Location Triggers as part of Autocuits Suite or download it individually from RoutineHub:

- [Download Autocuts Suite Installer](https://routinehub.co/shortcut/3661)
- [Download Location Triggers](https://routinehub.co/shortcut/3620)

Autocuts Suite contains the following shortcuts:

- [Autocuts](https://routinehub.co/shortcut/3606)
- [Autocuts Admin](https://routinehub.co/shortcut/3607): Create, manage, and view your Autocuts.
- [LimitKit](https://routinehub.co/shortcut/3603): Event logging and rate limiting so that Location Triggers is not constantly pinging your current location.

****

## Interface
Here is a quick overview of Location Triggers' interface. There are three primary screens:

### Home
This is the screen that you see when you first open the shortcut.

- **New Location Trigger**: Create a new location trigger.
- **View Location Triggers**: Tap to go to the list view.
- **Run**: Evaluate your location triggers and run any shortcuts whose location triggers match your current location.
- **About**: Includes the current version and build number.
- **Help**: Opens up to the document you are reading now.
- **Settings**: Adjust the settings of Location Triggers.

### List
Tapping on the View Location Triggers menu item retrieve any location triggers that you have saved.

- **List of location triggers**
- **Filter**: You can add tags to your location triggers for easy search later on.
- **New Location Trigger**
- **Run**: Evaluate your location triggers. Running it from the Home screen will always work, even if you have turned on LimitKit support.
- **Bulk Edit and Bulk Edit All**: Enable, disable, or delete multiple location triggers at once.

> Note: Location triggers are stored in `iCloud Drive/Shortcuts/Location Triggers`

### Location Trigger Detail
This view is displaying when you tap on a location triggers. Each location trigger can modify the following things:

- **Location Trigger Toggle**: The on/off switch for this location trigger.
- **Name**: The name of a location trigger.
- **Location**: The 
- **Trigger Radius**: The distance in miles or kilometers from the center of the location. If you fall within the radius, your shortcuts try to run.
- **Shortcut**: The shortcut that will run when you arrive or leave a location.
- **Shortcut Input**:
- **Active Time**: Restrict this location trigger between a start and finish time.

![Location Trigger Detail](https://adamtow.github.io/location-triggers/images/location-trigger-detail.png)

****

## Creating a Location Trigger
There are a number of ways to create a location trigger:

1. Use the Location Trigger Assistant.
2. Use the [New Location Trigger From Input shortcut](https://routinehub.co/shortcut/3658) from the iOS Share Sheet to identify locations in text, web pages, contacts, maps, and more.

### Location Trigger Assistant
In this example, we're going to create a location trigger centered around Apple's new campus.

1. Tap **Location Triggers** from the Shortcuts Home screen.
2. Tap **New Location Trigger**.
3. Tap **When I Arrive** to create an arrival trigger.
4. Enter the address to center the trigger. Here we are choosing Apple Park, located at One Apple Park Way in Cupertino, CA.\
\
![Location Trigger Assistant #1](https://adamtow.github.io/location-triggers/images/location-trigger-example-1.png)

5. Enter the trigger radius. For this example, we'll choose a very generous 100 kilometer radius around Apple Park.
6. Choose the shortcut that will run you are within 100 kilometers of Apple Park. 
7. Select any input to send to the shortcut. In this case, Auto Notification takes text input.\
\
![Location Trigger Assistant #2](https://adamtow.github.io/location-triggers/images/location-trigger-example-2.png)

8. Enter the text, `"I am within 100 kilometers of Apple Park!"` that will be sent to the Auto Notification shortcut.
9. Choose when this location trigger should be active.
10. Select what should happen after the location trigger successfully fires.\
\
![Location Trigger Assistant #3](https://adamtow.github.io/location-triggers/images/location-trigger-example-3.png)

11. Name your location trigger.
12. Finally, switch to another application and watch your shortcut run successfully in the background based on your location. No tapping of a confirmation button required!\
\
![Location Trigger Assistant #4](https://adamtow.github.io/location-triggers/images/location-trigger-example-4.png)

### Share Sheet
Use the [New Location Trigger From Input shortcut](https://routinehub.co/shortcut/3658) from the iOS Share Sheet to import new locations as location triggers. The shortcut can extract locations from contacts, text, Safari Web Pages, and Maps links.

![New Location Trigger From Input screenshot](https://adamtow.github.io/location-triggers/images/new-location-trigger-from-input.png)

****


## Frequently Asked Questions

### The Shortcuts notification that it is running an automation is very distracting. Is there any way to get rid of it?
Yes, it is annoying. Unfortunately, there's no way to disable the notification, as it is controlled by iOS. File feedback with Apple using their [Feedback Assistant system](https://feedbackassistant.apple.com).

### What's the difference between Get Current Location and Get Current Weather?
Get Current Location is slower but more accurate. Get Current Weather is faster, but potentially less accurate. The former will also have an impact on battery life, as it will have to power up the GPS radios to pinpoint your location.

Consider setting your LimitKit settings so that Location Triggers is only checking your location every 15 minutes instead of 5 minutes.