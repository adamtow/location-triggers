# Location Triggers
Location Triggers is part of Autocuts Suite, a collection of shortcuts that greatly enhance the automation abilities on iOS 13. It works with [Autocuts](https://adamtow.github.io/autocuts-admin) to automatically run shortcuts in the background based on your location while you use your iOS device — no need to tap on a button in a notification!

![Location Triggers](https://adamtow.github.io/location-triggers/images/location-triggers-screens.png)

## Why Location Triggers
iOS 13.1 brought about personal automations to Shortcuts, allowing users to create shortcuts that can run at certain times and locations. Unfortunately, these triggers require the user to tap on a confirmation button in order for shortcuts to run. Location Triggers was developed to remove this restriction until Apple decides to make the confirmation an optional requirement in iOS.

****

<span id="download"></span>
## Download Location Triggers
You can get Location Triggers as part of Autocuts Suite or download it individually from RoutineHub:

- [Download Autocuts Suite Installer](https://routinehub.co/shortcut/3661)
- [Download Location Triggers](https://routinehub.co/shortcut/3620)

Autocuts Suite contains the following shortcuts:

- [Autocuts](https://routinehub.co/shortcut/3606)
- [Autocuts Admin](https://routinehub.co/shortcut/3607): Create, manage, and view your Autocuts.
- [LimitKit](https://routinehub.co/shortcut/3603): Event logging and rate limiting so that Location Triggers is not constantly pinging your current location.

> **NOTE**: In order to use Location Triggers in an automatic fashion, you must install Autocuts and Autocuts Admin.

### What is Autocuts and What are Autocuts?
Autocuts is a background shortcut manager that works on top of Open App personal automation feature of Shortcuts in iOS 13. Choosing your most commonly used applications to launch Autocuts in the background ensures that your automated shortcuts are constantly working behind the scenes to do things like:

- Set Do Not Disturb for specific calendar events.
- Turn on Low Power Mode when your battery falls below a certain percentage.
- Send text messages, emails, or web requests at certain times of the day or when you arrive or leave locations.

****

<span id="interface"></span>
## Interface
Here is a brief overview of Location Triggers' interface. There are three primary screens:

### Home
This is the screen that you see when you first open the shortcut.

- **New Location Trigger**: Create a new location trigger.
- **View Location Triggers**: Tap to go to the list view.
- **Run**: Evaluate your location triggers and run any shortcuts whose location triggers match your current location.
- **About**: Includes the current version and build number.
- **Help**: Opens up to the document you are reading now.
- **Settings**: Adjust the settings of Location Triggers.

![Location Trigger Detail](https://adamtow.github.io/location-triggers/images/location-triggers-screens.png)

### List
Tapping on the View Location Triggers menu item retrieve any location triggers that you have saved.

- **List of location triggers**
- **Filter**: You can add tags to your location triggers for easy search later on.
- **New Location Trigger**
- **Run**: Evaluate your location triggers. Running it from the Home screen will always work, even if you have turned on LimitKit support.
- **Bulk Edit and Bulk Edit All**: Enable, disable, or delete multiple location triggers at once.

![Location Trigger Detail](https://adamtow.github.io/location-triggers/images/location-triggers-list.png)

> Note: Location triggers are stored in `iCloud Drive/Shortcuts/Location Triggers`

### Location Trigger Detail
This view is displaying when you tap on a location triggers. Each location trigger can modify the following things:

- **Location Trigger Toggle**: The on/off switch for this location trigger.
- **Name**: The name of a location trigger.
- **Location**: The location to be monitored. 
- **Trigger Radius**: The distance in miles or kilometers from the center of the location. If you fall within the radius, the shortcut specified in the location trigger will run.
- **Shortcut**: The shortcut that will run when you arrive or leave a location.
- **Shortcut Input**: The text input to send to the shortcut.
- **Active Time**: Restrict this location trigger between a start and finish time during the day.
- **LimitKit Run Interval**: When LimitKit support is enabled, you can set how long a location trigger must wait to be re-evaluated after a successful run. By default, location triggers are evaluated every time Location Triggers runs. Setting a run interval can save time if you are evaluating many location triggers or if you only need to run a shortcut once a day.
- **On Success**: What happens after a successful evaluation. Options include:
	- **Nothing**: Location Triggers will wait until you leave (for arrival triggers) or arrive (for leaving triggers) before it can re-evaluate the trigger.
	- **Disable**: The location trigger will be disabled after running the shortcut. You will have to manually re-enable it for it to work again.
	- **Reset**: Removes the previous location check, allowing the location trigger to run again at the next evaluation period. This is useful when debugging and troubleshooting an arrival location trigger since the shortcut will fire every time you are within the trigger radius.
	- **Delete**: Deletes the location trigger after running its shortcut. This operation cannot be undone.
- **Tags**: Add tags to your location triggers so you can filter them from the List screen.

![Location Trigger Detail](https://adamtow.github.io/location-triggers/images/location-trigger-detail.png)

****

<span id="new-location-trigger"></span>
## Creating a Location Trigger
There are a number of ways to create a location trigger:

1. Use the Location Trigger Assistant.
2. Use the [New Location Trigger From Input shortcut](https://routinehub.co/shortcut/3658) from the iOS Share Sheet to identify locations in text, web pages, contacts, maps, and more.

### Location Trigger Assistant
In this example, we're going to create a location trigger centered around Apple's new campus.

1. Tap **Location Triggers** from the Shortcuts Home screen.
2. Tap **New Location Trigger**.
3. Tap **When I Arrive** to create an arrival trigger.
4. Enter the address to center the trigger. Here we are choosing Apple Park, located at One Apple Park Way in Cupertino, CA.
5. Enter the trigger radius. For this example, we'll choose a very generous 100 kilometer radius around Apple Park.
6. Choose the shortcut that will run you are within 100 kilometers of Apple Park. 
7. Select any input to send to the shortcut. In this case, Auto Notification takes text input.
8. Enter the text, `"I am within 100 kilometers of Apple Park!"` that will be sent to the Auto Notification shortcut.
9. Choose when this location trigger should be active.
10. If you have [LimitKit support enabled](#limitkit), an option will appear to set a custom run cadence for the location trigger. 
11. Select what should happen after the location trigger successfully fires.
12. Name your location trigger.
13. Finally, switch to another application and watch your shortcut run successfully in the background based on your location. No tapping of a confirmation button required!

![New Location Trigger Assistant #1](https://adamtow.github.io/location-triggers/images/location-trigger-example-1.png)

![Selecting the trigger radius, shortcut, and input](https://adamtow.github.io/location-triggers/images/location-trigger-example-2.png)

![Configuring other location trigger options](https://adamtow.github.io/location-triggers/images/location-trigger-example-3.png)
 
![Saving the Location Trigger and running](https://adamtow.github.io/location-triggers/images/location-trigger-example-4.png)

### Share Sheet
Use the [New Location Trigger From Input shortcut](https://routinehub.co/shortcut/3658) from the iOS Share Sheet to import new locations as location triggers. The shortcut can extract locations from contacts, text, Safari Web Pages, and Maps links.

![New Location Trigger From Input screenshot](https://adamtow.github.io/location-triggers/images/new-location-trigger-from-share.png)

****

<span id="adding-to-autocuts"></span>
## Adding Location Triggers to Autocuts
To realize the full potential of Location Triggers, it must be added as an Autocut using Autocuts Admin. Follow these steps to accomplish this:

1. Open **Autocuts Admin** from the Shortcuts Home screen.
2. Tap **New Autocut**.
3. Choose **Location Triggers** from the list of shortcuts.
4. Tap **No Input**.
5. Tap **Run in Background**.
6. Tap **OK** since we want Location Triggers to start running immediately.
7. Tap **Never Expire**.
8. If [LimitKit](#limitkit) is enabled, you can adjust the run cadence for Location Triggers here.
8. Tap **Nothing**.
9. Tap **This Device**.
10. Enter a descriptive name for your Autocut and tap OK.
11. Tap the the iCloud (Your Device Name) destination service.

![Adding Location Triggers to Autocuts (1/3)](https://adamtow.github.io/location-triggers/images/location-triggers-autocut-1.png)

![Adding Location Triggers to Autocuts (2/3)](https://adamtow.github.io/location-triggers/images/location-triggers-autocut-2.png)

![Adding Location Triggers to Autocuts (3/3)](https://adamtow.github.io/location-triggers/images/location-triggers-autocut-3.png)

****

<span id="limitkit"></span>
## LimitKit
LimitKit is an event logging system and rating limiting tool for shortcuts. Location Triggers takes advantage of LimitKit to control how often your location triggers can run their shortcuts.

Location Triggers works with LimitKit and allows you to run the shortcut in a location trigger at intervals of seconds, minutes, hours, days, weeks, months, or even years. For instance, you can create a daily location trigger that marks your location in the world once a day. This is useful if you travel frequently and want to keep track of where you've wake up on a daily basis.

LimitKit support is enabled in the Settings page of Location Triggers.

![LimitKit settings and sample location trigger](https://adamtow.github.io/location-triggers/images/location-triggers-limitkit.png)

****

<span id="advanced"></span>
## Advanced

### Location Wildcard
When entering the location for a location trigger, you can specify `*` to represent your current location. This will cause the trigger to be successfully matched as long as you move outside of the trigger radius that you specify. This allows for intriguing shortcut possibilities such as calculating how often you leave your home area or logging where you wake up each day.

### Order of Precedence
When evaluating a location trigger, these checks are made in the following order:

1. Autocuts - Scheduled Date for Location Triggers
2. Autocuts - Expiration for Location Triggers
3. Autocuts - LimitKit for Location Triggers
4. Active Status
5. Time Range
6. LimitKit
7. Location Validity
8. Arrive or Leave
9. Location Wildcard
10. Distance from Current Location and Trigger Location

Keep this in mind as you develop location triggers with Autocuts Suites.

### API
You can send a Location object to Location Triggers in order to programatically open the Location Trigger Assitant and start creating a new location trigger.

****

<span id="localization"></span>
## Localization
Today, Auto DND is localized for the English language, but it's ready to be localized in any supported language by iOS. Please visit [Auto DND's GitHub page](https://github.com/adamtow/auto-dnd/tree/master/localization) and submit a pull request with a new localization file.

****

<span id="faq"></span>
## Frequently Asked Questions

### The Shortcuts notification that it is running an automation is very distracting. Is there any way to get rid of it?
Yes, it is annoying. Unfortunately, there's no way to disable the notification, as it is controlled by iOS. File feedback with Apple using their [Feedback Assistant system](https://feedbackassistant.apple.com).

### What's the difference between Get Current Location and Get Current Weather?
Get Current Location is slower but more accurate. Get Current Weather is faster, but potentially less accurate. Get Current Location will also have a more negative impact on battery life, as it forces your iOS device to power up the GPS radios to pinpoint your location.

