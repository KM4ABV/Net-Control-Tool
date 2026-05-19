# Net Control Tool

## Short Summary

**Net Control Tool** is a single-file, browser-based amateur radio net control assistant designed to help net controllers manage live check-ins, maintain a master roster, track station reports, record UTC times, organize traffic, view mapped stations, monitor propagation, and print professional tactical reports.

It was built for amateur radio operators who want a clean, fast, and practical tool that works during real nets without requiring a complicated installation, database server, or paid software package. The program runs from one HTML file, stores data locally in the browser, and includes features for both casual social nets and more structured emergency, training, or club operations.

Created by **KM4ABV Alexander Appel**.

---

# Detailed Program Description

**Net Control Tool** is a purpose-built net management dashboard for amateur radio operators who serve as net control stations. It is designed to replace paper check-in sheets, scattered notes, copied rosters, and improvised spreadsheets with one organized interface that can be used during an active net.

The program gives the net controller a live operating screen with a permanent **Master Roster** on one side and a working **Current Session Checklist** on the other. Stations can be added by callsign, organized in order, marked as mobile, logged with signal reports, given weather and traffic notes, tracked with UTC start and end times, and saved into a long-term station history.

The goal is simple: make net control work faster, cleaner, and easier while preserving useful history for future nets.

This tool is especially useful for:

* Nightly social nets
* Club nets
* Emergency communications practice nets
* ARES, RACES, CERT, or community preparedness nets
* Training nets
* Traffic handling practice
* Repeater group nets
* Linked repeater system nets
* Special event or public service radio operations
* Operators who want searchable historical check-in records

The program is intentionally simple to distribute. It is a single HTML file that opens in a browser. There is no installer, no local server, no external database, and no complicated setup. Data is saved locally in the browser, and the database can be exported or imported as a backup file.

---

# Core Concept

The program is built around two major ideas:

## 1. Master Roster

The **Master Roster** is the long-term database of stations. Once a station is added, its information can be reused on future nets.

The roster can store:

* Callsign
* Operator name
* License or profile type
* Address or QTH note
* Latitude and longitude
* First seen date
* Total check-in days
* Last check-in history
* Signal reports
* Weather reports
* Traffic or message notes
* Comments and operator memos
* QRZ lookup status
* Manual profile data

If a station checks in again later, the tool can instantly reuse the saved profile, even when internet or QRZ access is unavailable.

## 2. Current Session Checklist

The **Current Session Checklist** is the active operating list for the net currently being run.

This is where the net controller works through check-ins, rearranges order, records reports, marks mobile stations, tracks start and end times, and saves station traffic.

Stations can be removed from the Current Session without deleting them from the Master Roster.

---

# Major Features

## Callsign Check-In System

The net controller can type a callsign and press Enter to add a station to the Current Session.

If the callsign already exists, the saved data loads immediately.

If the callsign is new, the program marks it as new and can attempt to populate information through QRZ when available.

New callsigns can be labeled with a small green `*New` indicator so the net controller can quickly identify first-time check-ins.

---

# QRZ Lookup Support

The tool supports QRZ-assisted lookup for station information.

When configured with QRZ credentials, the program can attempt to retrieve station details such as:

* Operator name
* Address or QTH
* License class
* Latitude
* Longitude

To reduce bottlenecks, QRZ sync is separated into two workflows:

## Sync New QRZ

This only searches for stations that have not previously been synced. It is intended for normal use during active nets so the program does not waste time refreshing stations that are already known.

## Full Database Sync

This option is located inside Settings. It refreshes the full roster and can overwrite manually entered data with QRZ data.

This separation helps keep the program responsive while still allowing the entire database to be updated when needed.

---

# Offline-Friendly Operation

The program can still be useful without internet access.

If QRZ is unavailable, previously saved station data can still be loaded from the local Master Roster. New stations can be manually added and edited.

The manual profile editor allows the user to enter:

* Name
* License or profile type
* Address or QTH
* Latitude
* Longitude

This makes the tool practical for field use, portable operations, emergency exercises, or poor internet conditions.

---

# Mobile Station Handling

Mobile stations can be marked with a checkbox.

By default, when a station is marked mobile, the program moves that station toward the top of the Current Session list. This helps the net controller work mobile stations earlier in case their signal drops while traveling.

This behavior can be disabled in Settings.

Mobile status is saved into the station history and appears in reports.

---

# Station Report Saving

Each current session station card includes fields for:

* Signal report, such as RST
* Weather report
* Traffic or message notes

After the net controller enters the report, clicking **Save Card** locks the report row, greys it out, and changes the button to **Edit Card**. This gives the operator a clear visual confirmation that the report was saved.

Saved reports are shown in the Master Roster as a clean summary, such as:

```text
Last Report [2026-05-19]: RST: 59 | WX: Clear | Traffic: All good
```

---

# UTC Timing

The tool includes detailed UTC time tracking.

## Per-Station UTC Times

Each station can have:

* UTC Start Time
* UTC End Time

Only the next active station shows a live ticking UTC clock. This prevents the screen from being cluttered with multiple moving clocks.

When the station begins speaking, the net controller can lock the start time. When the station finishes, the net controller can lock the end time.

Times include seconds and are saved into the station history.

## Session-Level UTC Times

The entire net session can also have a Start UTC and End UTC time. These are opened with a clock button next to the Current Session Checklist title.

The start and end clocks operate independently. Locking the session start time does not stop the session end clock from continuing to run.

Session start and end times are saved indefinitely and are included on tactical reports.

---

# Session Summary

The tool includes a session summary editor.

The net controller can write a summary of the net, including:

* Net purpose
* General comments
* Number of check-ins
* Emergency or priority traffic
* Frequency changes
* Propagation notes
* Training observations
* Closing remarks

When the session end time is locked, the program reminds the net controller to complete a session summary.

The summary can optionally print as its own final page on the tactical report.

---

# Net Controller Station

The program has a dedicated **Net Controller Station** setting.

When a net controller callsign is set:

* The callsign appears near the Current Session Checklist title
* The callsign is highlighted in red in the roster and session list
* The NCO station appears as a large red dot on the map
* The map can draw lines from the NCO station to known stations
* Hovering over the NCO marker identifies the net controller station

This makes it easy to visually separate the controlling station from other stations in the net.

---

# Mapping System

The Map tab provides a visual view of stations with known latitude and longitude.

The map can filter by:

* Current Session
* Today’s Visitors
* This Week
* Last 30 Days
* All Operators

The map includes:

* Station pins
* A red NCO marker
* Optional NCO-to-station distance lines
* Distance and bearing information
* Sidebar station list
* Live updates while the session changes

There is also an offline distance grid mode. This does not require map tiles. It plots stations by calculated distance and bearing from the NCO location using saved latitude and longitude.

The map can be printed by itself without printing the rest of the program.

---

# Propagation Tab

The Propagation tab displays solar-terrestrial data from HamQSL.

This gives net controllers quick access to propagation information without leaving the tool.

This feature requires internet access.

---

# Tools Menu

The program includes a Tools menu for quick reference utilities.

## Script Tool

The Script tool provides a saved editable script area.

It can be used for:

* Net opening scripts
* Net closing scripts
* Emergency net language
* Repeater announcements
* Club announcements
* Standardized roll call language

The script is saved locally.

## Band Plan Map

The Band Plan Map opens a zoomable reference image for amateur radio band allocations.

It includes:

* Zoom in
* Zoom out
* Close

## US Call Map

The US Call Map opens a zoomable U.S. call district map.

It includes:

* Zoom in
* Zoom out
* Close

---

# ID Timer

The built-in ID timer helps remind the net controller when to identify.

It can be enabled, disabled, or adjusted in Settings.

When the timer expires, the program alerts the net controller.

This is helpful during long nets where it is easy to lose track of time while managing check-ins and traffic.

---

# Tactical PDF Reports

The program includes a print-ready tactical report system.

Reports can include:

* Net date
* Net controller station
* NCO coordinates
* Frequency
* Mode
* Session Start UTC
* Session End UTC
* Check-in order
* Callsign
* Operator details
* Address or QTH
* Range and bearing
* Routine, mobile, or emergency status
* RST or signal report
* Weather report
* Tactical message or traffic
* Individual station Start UTC
* Individual station End UTC
* Optional session summary page

Reports can be printed or saved as PDF using the browser print dialog.

---

# Data Import and Export

The program supports database backup and transfer.

## Export Data

Exports the saved database to a JSON file.

This can be used for:

* Backups
* Moving the roster to another computer
* Sharing a net database between operators
* Preserving historical records

## Import Data

Imports a previously exported JSON file.

This can restore:

* Master Roster
* Current Session
* Station history
* Session details
* Archived reports
* Summary data

---

# Safety Features

The program is designed to reduce accidental data loss.

The visible clear button only clears the Current Session. It does not delete the Master Roster.

The dangerous database wipe option is hidden inside Settings and requires confirmation.

This helps prevent the operator from accidentally destroying the long-term roster during a live net.

---

# Help System

The program includes a Help button in the top right area.

The Help popup includes a searchable operating guide so users can quickly find instructions by keyword.

This makes the tool easier to distribute to operators who have never used it before.

---

# Who This Is For

This tool is ideal for:

* Ham radio clubs
* Repeater associations
* Net control operators
* Emergency communications groups
* ARES and RACES teams
* CERT radio groups
* Public service event communicators
* Linked repeater net operators
* Amateur radio instructors
* Operators who run nightly or weekly nets

It is especially useful for operators who want a better way to track who checked in, what they said, when they spoke, where they are located, and how often they participate.

---

# Why It Is Useful

Traditional net control logging often relies on paper, spreadsheets, or memory. That can work for small nets, but it becomes harder as participation grows, especially when operators want to track history, manage mobile stations, document traffic, or print formal reports.

This tool brings those functions together in one interface.

It helps the net controller:

* Move faster during roll call
* Keep better records
* Avoid losing station history
* Prioritize mobile stations
* Track emergency traffic
* Save signal and weather reports
* Document session times
* Print clean tactical reports
* Maintain a permanent roster
* Use saved data when offline
* Visualize station locations
* Share or back up the database

---

# Simple Distribution

The program is distributed as a single HTML file.

Users can:

1. Download the file
2. Open it in a browser
3. Configure Settings
4. Start checking in stations

No installation is required.

No server is required.

No separate database is required.

The user remains in control of their own local data.

---

# Suggested Upload Description

**Net Control Tool** is a single-file amateur radio net control dashboard for managing live check-ins, master rosters, QRZ-assisted station lookups, mobile stations, signal reports, weather reports, traffic notes, UTC timing, session summaries, station maps, propagation references, and printable tactical PDF reports.

It was designed for ham radio net controllers who want a practical, easy-to-run logging and coordination tool without installing a full software suite. It works from one HTML file, stores data locally, supports import/export backups, and includes offline-friendly manual station profiles.

Use it for club nets, social nets, repeater nets, training nets, emergency communications practice, and public service radio operations.

Created by **KM4ABV Alexander Appel**.
