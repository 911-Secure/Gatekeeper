# Gatekeeper
The public release point for Sentry Gatekeeper.

## Release Notes

### 0.1.17
- Minor UI changes as we prepare for public release

### 0.1.16
- Fixed a packaging issue that prevented 0.1.15 from working
- Fixed issues with tooltips not rendering properly

### 0.1.15 (DO NOT USE)
- This version cannot start or update on its own. If you have this version, manually update 0.1.16 or newer.
- Replaced the network detection with a simpler and faster IP-based method
- Enabled pre-release auto-updating for those running a pre-release version. It will not upgrade from a stable version to a pre-release version.
- Fixed an issue with auto-launch on Mac

### 0.1.14
- Disabled process detection to improve performance
- Standardized terminology
- Added a redirect to the addresses page if the address is unknown
- UI changes to make the selected address more visible
- Added an auto-start feature to launch Gatekeeper on login
- Added tooltips and other hints

### 0.1.13
- Minor typos and corrections

### 0.1.12
- Handle Duplicate ELIN.
- Keep application running even if Window closed (Windows).
- Warn users of available upgrade.
- Splash screen obscured by license dialog (Windows).

### 0.1.11
- New app icon.
- New licensing model with Azure AD.
- Detect network change prompts location request.
- Fix map pin detail.
- About box.
- Local logging.
- Monitor processes for soft phone launch.
