# Sentry Gatekeeper
The public release point for Sentry Gatekeeper.

## Release Notes

### 1.2.28
- **Public Release**

#### Revisions

- Resolved the issue with the full list of local WiFi networks not always being returned
- Cleaned up the UI in various places
- Updated various pieces of informative text

### 1.2.25
- **Public Release**

#### Known Issue

- Currently, when Gatekeeper asks Windows for the list of local WiFi networks (from clicking on Find Me on Map, when trying to geolocate the user), only the user's own WiFi network may be returned if WiFi polling on Windows has been suspended. With just a single WiFI network, a large probability radius from Find Me on Map may be seen.  To improve results, first click on the WiFi symbol in the taskbar notification area.  Then, when more than just the user's own WiFi network is displayed, click on File -> Find Me on Map in Gatekeeper to receive improved results.  The next release of Gatekeeper will force a refresh from Windows of all local WiFI networks so this extra step will not be necessary.

#### Revisions

- Added enhanced logging
- Updated Network Status page with additional URL needing to be whitelisted
- Added code to send to Internet Connection Required page if Google APIs cannot be reached
- Added additional text to accuracy radius popup to prompt user to suggest refreshing WiFi connections

### 1.2.24
- **Public Release**

#### Revisions

- First public version of Gatekeeper for macOS
- Improved network detection (WiFi, LAN, airplane mode, etc.)
- Fixed an issue where some screens appeared blank (white) on startup

### 1.2.23
- **Public Release**

#### Revisions

- Gatekeeper no longer prompts users to set their location upon a restart if they haven't changed networks / locations.  It will do this one last time if running an earlier version.
- Updated the way addresses are stored in Gatekeeper.  If an earlier version was run, its recommended you delete all current saved addresses and then re-add them.
- Improved UI / workflow to make it more intuitive.  Starting always from Locations, users can either click "Find Me on Map" if in a good place with surrounding WiFi antennas for geolocation, or else they can click the + sign in the bottom left corner to add a new address manually.
- There is currently a 5 minute grace period before displaying a hard “Internet Connection Required” message on the screen.  A small popup message is first displayed, asking the user to check their internet if they clicked on Find Me on Map and no internet is available.

### 1.2.12
- **Public Release**

#### Revisions
- Fix a bug preventing display of address list when Dispatcher records had been cleared
- Removed Map menu item from tray menu


### 1.2.11
- **Public Release**

#### Revisions
- Cancel web service requests that take longer than 10 seconds, to help with unstable network connections
- More javascript exceptions being trapped now


### 1.2.10
- **Public Release**

#### Revisions
- Better handling of slow networks and connect/disconnect
- Pause after detecting a restoration of network connection before enabling the app


### 1.2.8
- **Public Release**

#### Revisions
- Detect network disconnection and notify user
- Better handling of changing networks and VPNs


### 1.2.1
- **Public Release**

#### Revisions
- Added code to prevent multiple instances of Sentry Gatekeeper from starting up.  Subsequent attempts to start Gatekeeper will bring users to the Locations page in the currently running Gatekeeper.


### 1.2.0
- **Public Release**: The first public release of Sentry Gatekeeper

#### Revisions
- Includes all bug fixes contained in prior beta releases
- Added location detection that uses nearby WiFi access points to determine a street address
- Inaccurate locations detected this way may be corrected and remembered for future visits
- Fixed a bug that can occur if Gatekeeper is launched without Internet access
- Users can now select addresses directly from the map. These addresses may be edited if necessary.
- Fixed a bug that prevented notifications from appearing in Windows 10
- Updated images and logos
- Reminds user to update their location/address every 2 mins if it detects a new network connection
- Changed the wording of network change notifications
- Added resiliency when Endpoints are deleted from Dispatcher
- Users are now shown the validated address before saving
- Added a link to the public release notes
