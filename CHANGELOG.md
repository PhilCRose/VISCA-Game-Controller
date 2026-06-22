# VISCA Game Controller Changelog

## Version 1.1beta1 (2026-06-21)

### Overview

This release adds significant usability improvements for Bitfocus Companion integration, camera management, and controller configuration while maintaining backward compatibility with previous versions.

### New Features

* Added configurable camera names.
* Camera names are persisted across application restarts.
* OSC `/setcam` command now accepts either:

  * Camera numbers (e.g. `1`)
  * Configured camera names (e.g. `Front`, `Left`, `Over`, `Tail`)
* Added OSC `/clearcam` command to disable PTZ control when no camera is active.
* Added configurable response profiles for:

  * Pan
  * Tilt
  * Zoom
  * Focus
* Added validation for response profile entries in the Configure dialog.
* Added Companion Help documentation accessible from the application menu.

### User Interface Improvements

* Reorganized the Configure dialog into logical sections:

  * Cameras
  * Controller
  * Speed Profiles
  * Companion
* Added support for descriptive camera names throughout the application.
* Added explanatory text for configurable speed profiles.

### Companion Integration

* Selecting a camera via `/setcam` automatically enables gamepad PTZ control.
* Sending `/clearcam` disables PTZ control until another `/setcam` command is received.
* Recommended use of camera names instead of numeric identifiers for improved readability and maintainability.

### Compatibility

* Existing numeric `/setcam` OSC commands remain fully supported.
* Existing Companion configurations continue to function without modification.

---

Original application by Dan Tappan.

Enhancements for Version 1.1beta1 by Phil Rose (Dragon's Rose Studio).
