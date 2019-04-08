# Sentry Gatekeeper
The public release point for Sentry Gatekeeper.

## Release Notes

### 1.2.1
- **Public Release**

#### Known Issue
- In rare circumstances, typing in a full address for a new or updated location does not invoke automatic validation.  In such a case, resizing the window (even slightly) resolves the issue and validation occurs.

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
