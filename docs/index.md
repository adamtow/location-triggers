# Location Triggers
Location Triggers works with Autocuts to automatically run shortcuts in the background based on your location while you use your iOS device.


## Creating a Location Trigger
There are a number of ways to create a location trigger:

1. Use the Location Trigger Assistant.
2. Send a Location as input to the Location Triggers shortcut.
3. Share a location from the Maps application.

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
Location Triggers accepts Locations from the share sheet. So, one can go into the Maps application, find a location, and assign an arrival or departure location trigger for that place.