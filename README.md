# Net Control Tool

A browser-based amateur radio net control logging tool for managing check-ins, maintaining a master roster, tracking tactical reports, printing net reports, viewing operator locations, and managing repeater information.

This public release is packaged as a single HTML file and does not require a server, installer, database, or internet connection for normal offline operation. Optional online features, such as QRZ lookups and online maps, require internet access and valid configuration.

> Public release note: this version does not include the Band Plan feature.

## Table of Contents

- [Overview](#overview)
- [Core Design](#core-design)
- [What This Tool Is For](#what-this-tool-is-for)
- [Quick Start](#quick-start)
- [Data Storage](#data-storage)
- [Main Screen Layout](#main-screen-layout)
- [Header Controls](#header-controls)
- [Settings](#settings)
- [NCO Callsign and Net Controller Station](#nco-callsign-and-net-controller-station)
- [QRZ Integration](#qrz-integration)
- [Online and Offline Mode](#online-and-offline-mode)
- [Current Session Checklist](#current-session-checklist)
- [Per-Log Station Reports](#per-log-station-reports)
- [UTC Start and End Times](#utc-start-and-end-times)
- [Session Clock](#session-clock)
- [Session Summary](#session-summary)
- [Master Roster](#master-roster)
- [Manual Profile Editing](#manual-profile-editing)
- [Regular Check In's Tab](#regular-check-ins-tab)
- [Transcript Tab](#transcript-tab)
- [Map Tab](#map-tab)
- [Repeater Tab](#repeater-tab)
- [CHIRP CSV Import and Export](#chirp-csv-import-and-export)
- [Propagation Tab](#propagation-tab)
- [Tools Menu](#tools-menu)
- [ID Timer](#id-timer)
- [Tactical PDF Report](#tactical-pdf-report)
- [Print Map](#print-map)
- [Scratchpad](#scratchpad)
- [Help System](#help-system)
- [Import and Export](#import-and-export)
- [Recommended Workflow](#recommended-workflow)
- [Best Practices](#best-practices)
- [Privacy and Data Notes](#privacy-and-data-notes)
- [Browser Compatibility](#browser-compatibility)
- [Known Limits](#known-limits)
- [Public Release Changes](#public-release-changes)
- [License](#license)

## Overview

Net Control Tool is designed to help a net control operator run an amateur radio net from a single browser window. It combines a current-session checklist, master roster, station history, tactical logging, maps, repeater management, QRZ lookups, printable reports, and a searchable help guide.

The tool is built as a standalone HTML application. The operator opens the file in a browser and uses it locally. Information is saved in the browser's local storage so the roster, settings, and logs can persist between sessions on the same computer and browser profile.

## Core Design

The application separates long-term station information from per-session and per-log information.

Long-term station information includes items such as:

- Callsign
- Operator name
- Address or QTH information
- QRZ profile details
- Latitude and longitude when available
- Grid square when available
- Profile memo notes
- Check-in history

Per-log information includes items such as:

- Signal report or RST
- Weather report
- Comment or tactical message
- UTC start time
- UTC end time
- Frequency, band, and mode
- Emergency traffic status
- Recheck status
- Mobile station status

This means a station can check in on multiple days with different signal, weather, and comment details without overwriting prior transcript entries.

## What This Tool Is For

This tool is useful for:

- Weekly amateur radio nets
- Emergency communications practice nets
- ARES, RACES, CERT, club, and community nets
- Tactical check-in logging
- Tracking operator participation over time
- Printing net reports
- Managing repeater lists
- Exporting repeater data for CHIRP
- Viewing station and repeater locations on a map

## Quick Start

1. Download the public-release HTML file.
2. Open the file in a modern desktop browser.
3. Open **Settings** and enter the NCO callsign at the top of the settings page.
4. Configure optional QRZ credentials if you want QRZ profile sync.
5. Enter a station callsign in the current session input box.
6. Add the station to the current session.
7. Enter signal, weather, and comments for that station's specific log entry.
8. Save the station report.
9. Print or archive the tactical report when the net is complete.

No installation is required.

## Data Storage

The tool stores data in the browser using local storage. This allows data to remain available after closing and reopening the browser on the same device and browser profile.

Stored information may include:

- Settings
- Master roster
- Station history
- Transcript records
- Repeater list
- QRZ profile data
- Scratchpad content
- Session metadata

Important notes:

- Local storage is tied to the browser and device.
- Clearing browser data may delete saved tool data.
- Opening the file in another browser may not show the same saved roster.
- Export backups are recommended before major edits, browser resets, or computer changes.

## Main Screen Layout

The application has three major areas:

### Header

The top header includes the application title, local and UTC clocks, Tools menu, online/offline toggle, QRZ connection status, ID timer, print controls, current session clearing, QRZ sync, help, and settings.

### Left Pane

The left pane contains tabbed tools:

- Roster
- Map
- Repeaters
- Regular Check In's
- Propagation
- Transcript

### Right Pane

The right pane contains the active current-session checklist. This is where the net control operator manages active check-ins and logs signal, weather, comments, time, mobile status, emergency traffic, and related per-session information.

## Header Controls

The header includes the following controls:

### Tools

Opens a dropdown containing utility tools such as the net script and US call map.

### Online or Offline Status

Switches between online and offline behavior. Online mode supports external services when configured. Offline mode allows the operator to continue using local data and offline-capable features.

### QRZ Status

Displays whether QRZ is connected, pending, warning, or not connected.

### ID Timer

Displays the station identification timer. The operator can reset it by clicking the timer button when the ID timer is enabled.

### Print Tactical PDF

Opens the print center for generating a tactical net report.

### Clear Current Session

Clears only the active current session checklist. It does not wipe the master roster.

### Sync New QRZ

Syncs only profiles that have not already been QRZ synced.

### Help

Opens the searchable help guide.

### Settings

Opens the settings modal.

## Settings

The settings page contains operational configuration for the tool. The NCO callsign box is placed at the top of the settings page so it can be found quickly.

Settings may include:

- NCO callsign
- QRZ username
- QRZ password
- Net controller station details
- NCO coordinates
- Session frequency
- Session mode
- ID timer settings
- Other tool preferences

Save settings after making changes.

## NCO Callsign and Net Controller Station

The NCO callsign identifies the net control station. This is used throughout the tool for reports, maps, and operating context.

The NCO station information may also be used as a mapping reference point when calculating approximate station distance and bearing.

## QRZ Integration

The tool includes optional QRZ integration for callsign lookup and profile enrichment.

QRZ features may include:

- Callsign profile lookup
- Operator name retrieval
- Address or QTH retrieval when available
- Grid square retrieval when available
- Coordinate retrieval when available
- License status display
- QRZ sync status indicator
- Manual sync of new unsynced callsigns

QRZ use requires internet access and valid QRZ configuration.

If QRZ is not configured, the tool can still be used manually.

## Online and Offline Mode

The online/offline toggle controls whether the tool should attempt online features.

### Online Mode

Online mode is intended for:

- QRZ profile syncing
- Online map loading
- External data that requires internet access

### Offline Mode

Offline mode is intended for:

- Local logging
- Roster access
- Transcript access
- Repeater list use
- Offline map behavior when available
- Continuity when internet service is unavailable

This is helpful for emergency communications and field use.

## Current Session Checklist

The current session checklist is the active working list for the current net.

Features include:

- Add callsigns to the current session
- Track checked and unchecked stations
- Mark station check-ins complete
- Edit callsigns if a typo was entered
- Reorder stations using a position dropdown
- Move stations up or down
- Remove a station from the current session
- Mark mobile stations
- Mark emergency traffic
- Save per-station tactical reports
- Support duplicate rechecks with confirmation
- Display log identifiers
- Show station metadata and profile information

The current session is separate from the master roster. Clearing the current session does not delete the master roster.

## Per-Log Station Reports

Signal report, weather, and comment fields are saved per log entry. They are not treated as permanent callsign profile fields.

This is important because the same operator may check in on different dates or at different times with different conditions.

Example:

| Date | Callsign | Signal | Weather | Comment |
| --- | --- | --- | --- | --- |
| Monday | KM4ABV | 59 | Clear | Good copy |
| Tuesday | KM4ABV | 33 | Windy | Weak signal, mobile |

These become separate transcript records. Updating one does not overwrite the other.

Per-log report fields include:

- RST or signal report
- Weather
- Comment or tactical message
- Start UTC
- End UTC
- Frequency, band, and mode when used
- Emergency traffic status
- Recheck information

## UTC Start and End Times

Each station card can track UTC start and end times.

Features include:

- Manual UTC entry
- Locking a start time
- Locking an end time
- Per-station time tracking
- Printed report support
- Transcript support

The start time and end time belong to the individual log entry.

## Session Clock

The session clock provides an additional way to track session-level timing. It can be used to keep a clear record of when station activity occurs during the net.

## Session Summary

The session summary allows the operator to write a summary of the net. This can be included in print output and archived with the session record.

Use it for:

- Net overview
- Emergency traffic notes
- Announcements
- Operational observations
- Issues encountered
- Follow-up items

## Master Roster

The master roster is the long-term station database.

Features include:

- Callsign list
- Operator details
- QRZ profile details
- Address or QTH information
- Distance and bearing information when coordinates are available
- Color-coded participation status
- Memo notes
- Profile editing
- QRZ links
- Delete station support
- Roster sorting
- Pagination support
- Check-in history summaries

Roster status colors indicate participation recency:

- Green: recently active
- Yellow: missed one week
- Red: missed two weeks
- Grey: other or unknown status

## Manual Profile Editing

Operator profiles can be edited manually. This is useful when QRZ data is missing, unavailable, outdated, or intentionally not used.

Editable information may include:

- Callsign
- Operator name
- Address or station location
- Coordinates
- Grid square
- Memo or notes
- Other profile details supported by the interface

Manual editing helps maintain accurate records even without internet access.

## Regular Check In's Tab

The Regular Check In's tab provides a snapshot of stations that regularly participate in the net.

It helps the net control operator quickly identify common participants and review their recent activity.

## Transcript Tab

The Transcript tab provides access to the full contact transcript archive.

Features include:

- Search transcript records
- View previous log entries
- Edit transcript fields
- Filter or review station reports
- Preserve per-log signal, weather, comment, and time details
- Maintain historical contact records

Transcript entries are identified independently so that repeated callsign check-ins remain separate records.

## Map Tab

The Map tab displays operator and repeater location information when coordinates are available.

Features include:

- Operator map view
- Station markers
- NCO reference marker
- Callsign labels
- Repeater map support
- Map filters
- Online map behavior
- Offline map behavior when available
- Popup map display
- Fullscreen map display
- Print map support

Map data quality depends on available station coordinates.

## Repeater Tab

The Repeater tab manages repeater information.

Features include:

- Starter repeater set
- Add repeaters
- Edit repeaters
- Delete repeaters
- Select multiple repeaters
- Export selected repeaters
- Export displayed repeaters
- Bulk delete selected repeaters
- Repeater map integration
- CHIRP CSV import
- CHIRP CSV export
- Scrollable repeater list

Repeater entries can be treated as an editable starter set rather than a hard-coded permanent list.

## CHIRP CSV Import and Export

The Repeater tab includes a consolidated **CHIRP CSV** dropdown.

Dropdown options:

1. IMPORT
2. EXPORT

### IMPORT

Imports repeater data from a CHIRP-compatible CSV file.

### EXPORT

Exports repeater data in CHIRP-compatible CSV format.

Export behavior supports the repeater list workflow, including exporting selected or displayed repeaters depending on the current interface state.

This dropdown keeps the Repeater tab cleaner while preserving CHIRP functionality.

## Propagation Tab

The Propagation tab displays radio propagation information to help the operator understand current signal conditions.

This can help explain poor copy, unusual band behavior, or improved propagation during a net.

## Tools Menu

The Tools menu contains utility tools.

Public-release tools include:

### Script

Opens the net script editor/viewer. Operators can use this for opening language, closing language, announcements, and net procedures.

### US Call Map

Opens the US call district map tool.

> Public release note: the Band Plan tool has been removed from this version.

## ID Timer

The ID timer assists with station identification timing.

Features include:

- Enable or disable timer behavior
- Timer status display
- Warning state
- Due state
- Manual reset by clicking the timer

This helps the net control operator remember periodic station identification requirements.

Operators are responsible for following applicable FCC and local operating rules.

## Tactical PDF Report

The Tactical PDF report feature prepares a printable report from the current net data.

Report content may include:

- Target log date
- Compiled timestamp
- NCO baseline information
- Session frequency and mode
- Check-in order
- Callsigns
- Operator details
- Station address or location information
- Range and bearing
- Status
- RST or signal report
- Start UTC
- End UTC
- Weather
- Tactical message or comment
- Emergency traffic indicators
- Session summary when included

The report is designed to support clean printed output from the browser.

## Print Map

The map print feature allows the operator to print a map-focused view. This can be useful for briefings, records, exercises, or post-net review.

## Scratchpad

The scratchpad is a quick note area for temporary net-control notes.

Use it for:

- Announcements
- Follow-up items
- Relay notes
- Temporary tactical notes
- Items to include in the session summary later

Scratchpad content may persist locally depending on browser storage behavior.

## Help System

The built-in help system is searchable and explains tool usage from inside the application.

Help topics include:

- Overview
- Starting the program
- Main screen layout
- Settings
- QRZ setup and sync
- Net controller station
- NCO coordinates
- Frequency and mode
- Adding stations to the current session
- Current session card controls
- Saving station reports
- UTC start and end times
- Session clock
- Session summary
- Master roster
- Manual profile editing
- Online and offline mode
- Map tab
- Repeater tab
- Printing the map
- Propagation tab
- Tools menu
- ID timer
- Tactical PDF report
- Import and export
- Clearing the current session
- Wiping the master roster
- Recommended workflow
- Best practices

## Import and Export

The tool includes import and export support for preserving data and moving information between installations or browsers.

Use exports before:

- Clearing browser data
- Moving to another computer
- Updating to a new version
- Major roster edits
- Public demonstrations
- Field deployments

## Recommended Workflow

1. Open the tool before the net begins.
2. Confirm the NCO callsign and session settings.
3. Confirm local and UTC time displays.
4. Confirm QRZ status if using online lookup.
5. Add stations as they check in.
6. Enter signal, weather, and comment details on each station card.
7. Save each station report.
8. Use emergency traffic marking when needed.
9. Use recheck confirmation for duplicate callsign entries.
10. Review the transcript before closing the net.
11. Add a session summary.
12. Print or save the tactical report.
13. Export backups as needed.
14. Clear the current session when ready for the next net.

## Best Practices

- Enter the NCO callsign before operating.
- Save each station report after entering tactical details.
- Use the transcript tab to verify historical entries.
- Export backups regularly.
- Do not clear browser data unless you have exported your records.
- Use offline mode when internet access is unreliable.
- Verify QRZ data manually when accuracy matters.
- Use notes and summaries for context that may not fit in short tactical fields.
- Test print output before relying on it during an event.
- Keep a backup copy of the HTML file and exported data.

## Privacy and Data Notes

This tool stores operational data locally in the user's browser. The public-release file itself does not require a central server.

Users should be aware that locally stored data may include station information, operator details, comments, and net records. Handle exported files appropriately.

QRZ data, if used, depends on the user's QRZ configuration and internet access.

## Browser Compatibility

Recommended browsers:

- Chrome
- Edge
- Firefox
- Brave

A desktop browser is recommended because the interface contains multiple panes, maps, forms, and printable report layouts.

## Known Limits

- Data is stored locally in the browser and can be lost if browser storage is cleared.
- QRZ features require valid QRZ setup and internet access.
- Online maps require internet access.
- Map accuracy depends on available coordinates.
- Print layout may vary slightly by browser and printer settings.
- This is a browser-based tool, not a multi-user cloud database.

## Public Release Changes

This public release removes the Band Plan feature.

The following features remain available:

- Current session checklist
- Master roster
- Per-log signal, weather, and comment reports
- Transcript archive
- Settings with NCO callsign at the top
- QRZ support
- Online and offline mode
- Map tab
- Map popup and fullscreen behavior
- Repeater tab
- CHIRP CSV dropdown with import and export
- Regular Check In's tab
- Propagation tab
- Tools menu with Script and US Call Map
- ID timer
- Tactical PDF report
- Scratchpad
- Searchable help guide

## License

Add your project license here.

Common options include:

- MIT License
- GNU General Public License
- Apache License 2.0
- Custom personal or club-use license

## Credits

Net Control Tool by KM4ABV.

