# Sentry Gatekeeper
The public release point for Sentry Gatekeeper.

## Release Notes

### 1.2.34
- **Public Release**

#### Revisions

- Fixed issues with saving and reloading of Locations

### 1.2.33
- **Public Release**

#### Revisions

- Fixed issue with the Map window's disclaimer interfering with the address on low resolution / high font scaling screens
- When clicking on the 5-minute reminder message, the address list page now opens
- Fixed issue with addresses sometimes not fully loading on startup and on network changes
- Updated installer to allow user-specific or machine-specific installations
- When a network change occurs, the user's ELIN entry in VPC is now deprovisioned
- The Internet Connection Required screen now shows only with user interaction after a network drop

### 1.2.32
- **Public Release**

#### Revisions
- In some cases, users were seeing the Internet Connection Required Screen at startup (some for a split second, some prolonged).  This has been corrected.
- Sometimes Gatekeeper would get hung up on loading the list of addresses.  This has been fixed.
- The Find Me on Map functionality now properly waits for the entire list of local WiFi antennas to be returned by Windows.  Previously, the call was made asynchronously and not all antennas were being passed to Google for geolocation.  The button functionality can now take as long as 5 or 6 seconds to locate the user, but it is now guaranteed to be the most accurate it can possibly be.

### 1.2.31
- **Public Release**

#### Revisions
- WakeWLAN.dll now targets .net 4.5.2, not .netstandard 2.0 (which caused problems on some computers)
- Users are alerted when Find Me on Map is used and the Wake WiFi could not be initialized
- Gatekeeper now starts with an open window to insure notification icon context menu is properly populated

### 1.2.30
- **Public Release**

#### Revisions

- Resolved the issue with the full list of local WiFi networks not always being returned
- Cleaned up the UI in various places
- Updated various pieces of informative text
- Removed the white screen seen during initial installation (users are directed to enter their Name and Phone Number)

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
