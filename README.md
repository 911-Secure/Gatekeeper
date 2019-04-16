# Sentry Gatekeeper
The public release point for Sentry Gatekeeper.

## Release Notes

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
