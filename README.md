Net Control Tool Description

Net Control Tool is a purpose-built amateur radio net management system designed for operators who want a clean, fast, and reliable way to manage check-ins, station records, tactical traffic, maps, logs, and reports from one simple self-contained HTML file.

Built with the real workflow of a net controller in mind, this tool combines the speed of a live checklist with the structure of a permanent station database. Operators can check stations in by callsign, automatically populate QRZ profile data when available, manually enter missing station details when offline, track signal reports, comments, emergency traffic, frequency, mode, time on/off, and preserve everything in an organized archive.

The interface is split into two practical work areas. The left side provides the Master Roster, live Map, and Propagation tools. The right side keeps the Current Session Checklist visible at all times, allowing the net controller to manage the active net without losing sight of who is next.

The program is intentionally simple to use and easy to preserve. It runs as a single HTML file, saves data locally in the browser, supports import and export backups, and does not require an installed server or complicated setup. It is ideal for hobby nets, club nets, emergency practice nets, training nets, and general amateur radio logging.

Feature Highlights
Current Session Management

The Current Session Checklist allows the net controller to quickly add callsigns, rearrange speaking order, remove stations from the active session without deleting them from the master roster, and track each station’s activity during the net.

Each station card can include:

Callsign
Operator name
License/profile type
Address or QTH note
QRZ profile link
Memo/comment button
Manual profile editor
RST report
Weather/status field
Tactical message field
Emergency traffic toggle
UTC start and end timing
Speaking order controls
Remove from current session option

Only the next active station displays a live UTC clock, keeping the interface clean and avoiding a screen full of moving clocks.

Master Roster Database

The Master Roster is the permanent station database. Once a station has checked in, its profile can be saved and reused in the future. If QRZ is unavailable or the station was previously registered, the tool can still populate saved information from local cache.

The roster stores:

Callsign
Operator name
License/profile type
Address/QTH
Latitude and longitude
Memo notes
First logged date
Last check-in date
Total check-in count
Historical session entries
Saved tactical traffic
Frequency and mode archive
UTC time records
QRZ Lookup and Sync

The tool supports QRZ lookup using the QRZ XML style workflow already familiar to many ham radio logging tools. QRZ lookups can populate station profile information such as name, address, license class, and coordinates when available.

To reduce bottlenecks, QRZ syncing is separated into two modes:

Sync New QRZ: only attempts to sync operators that have not already been synced.
FULL Database Sync: refreshes the full master roster and can overwrite manually entered data.

This avoids unnecessary repeated QRZ calls during active net control operations.

Offline-Friendly Operation

If QRZ is unavailable, or the operator is working without internet, the tool still functions. Stations can be manually added with name, profile type, address, latitude, and longitude. Once QRZ is available again, a full sync can refresh and overwrite the locally entered profile data.

Net Controller Station

The tool allows the net controller’s callsign to be configured in Settings.

When set:

The NCO callsign appears next to the Current Session Checklist.
The NCO is highlighted in red text in the roster and session list.
The NCO appears as a large red dot on the map.
Hovering over the red NCO dot shows the net controller callsign.
Distance lines can be drawn from the NCO station to all known mapped stations.
Live Map

The Map tab displays station locations using saved latitude and longitude data. It supports filtering by:

Current Session
Today’s Visitors
This Week
Last 30 Days
All Operators

The map includes:

Operator pins
NCO red dot
Optional NCO-to-station distance lines
Hover distance information
Sidebar station list
Live updates as new callsigns are added
Online map tiles
Offline distance grid fallback

The map can also be printed by itself without printing the rest of the app.

Propagation Tab

The Propagation tab displays solar-terrestrial data from HamQSL, giving operators a quick view of current band conditions without leaving the tool.

Tools Menu

The Tools menu includes utility features for net operations.

Current tools include:

Script: editable and saved locally, useful for net preambles, closing announcements, or standardized language.
Band Plan Map: opens a zoomable band allocation image for quick reference.
ID Timer

The built-in station identification timer helps remind the net controller when it is time to identify. It can be enabled, disabled, or adjusted from Settings.

Session Clock and Summary

The tool supports a session-level UTC start and end clock. The session clock is accessed with the clock emoji next to the Current Session Checklist title.

The session summary is accessed through the notepad emoji. The summary can be saved and optionally printed as its own final page in the tactical report.

When the session end time is checked, the tool prompts the net controller to complete a session summary.

Tactical PDF Report

The tactical report system creates a print-ready record of the session. It can include:

Date
Net controller station
NCO coordinates
Frequency
Mode
Session start and end UTC
Check-in order
Callsigns
Operator details
Address/QTH
Range and bearing
Status
RST
Weather
Tactical message
Emergency traffic indicator
Individual station UTC start and end times
Optional session summary on its own page
Data Safety

The tool includes several protections against accidental data loss.

Clearing the visible session only clears the Current Session.
Wiping the entire database is hidden in Settings.
The database wipe requires strong confirmation.
Import and export are available in Settings for backups.
The Master Roster is not affected when removing someone from the Current Session.
Net Control Tool Operating Manual
1. Starting the Program

Open the HTML file in your browser. No installation is required.

Recommended browser:

Chrome
Edge
Firefox

The app saves data locally in the browser using local storage. For best results, keep using the same browser and same computer unless you export and import your database.

2. Main Screen Layout

The screen is divided into two main sections.

Left Side

The left side contains tabs:

Roster
Map
Propagation
Right Side

The right side contains the Current Session Checklist.

This is where active check-ins are managed during the net.

3. Settings

Click Settings in the top bar.

Settings may include:

QRZ username
QRZ password
NCO latitude
NCO longitude
Net Controller Station
Session frequency
Session mode
ID timer settings
Map line settings
Print summary option
Import data
Export data
Full database sync
Wipe database

The Settings window can scroll if the screen is small.

4. QRZ Setup

Open Settings.

Enter:

QRZ Username
QRZ Password

Click Save Configuration.

If the credentials are accepted, the scratchpad log will show that QRZ authentication succeeded.

5. Setting the Net Controller Station

Open Settings.

Find Net Controller Station.

Enter your callsign.

Save settings.

The tool will:

Add or update the net controller station.
Attempt a QRZ lookup if the callsign has not already been synced.
Highlight that callsign in red wherever it appears.
Mark that callsign as the red NCO dot on the map.

If QRZ is unavailable, the tool keeps a local placeholder that can be manually edited.

6. Setting Frequency and Mode

Open Settings.

Enter:

Current Frequency
Current Mode

Examples:

146.520 MHz
147.240+
7.268 MHz
FM
USB
LSB
D-STAR
Fusion

Save settings.

This information is archived and included in tactical reports.

7. Adding a Station to the Current Session

On the right side, type a callsign into the callsign input field.

Press Enter.

The station will be added to the Current Session Checklist.

If the callsign already exists in the Master Roster, cached data is used immediately.

If QRZ is available, the tool may attempt to populate station information.

If QRZ is not available, the station can still be used as a local profile.

8. Current Session Checklist Controls

Each station in the Current Session may include several controls.

Checkbox

Used to mark the station as checked or completed.

Up and Down Arrows

Move the station higher or lower in the Current Session order.

Remove from Current Session

Removes the station from the Current Session only.

This does not delete the station from the Master Roster.

Emergency Button

Marks the station as emergency traffic.

Emergency traffic is visually highlighted and appears in the tactical report.

Comment Button

The speech bubble button opens the operator memo/comment editor.

Use this for notes about the station or operator.

Profile Editor

The pencil button opens manual profile editing.

Use this to enter or correct:

Name
License/profile type
Address/QTH
Latitude
Longitude

Manual data can later be overwritten by a Full Database Sync.

QRZ Link

Opens the station’s QRZ profile page.

9. UTC Start and End Times for Each Station

Each active station can have a UTC start and end time.

Only the next active station shows the live ticking UTC clock.

This prevents multiple clocks from moving at the same time.

Start UTC

When the station begins speaking, check the box next to the start time.

This stamps and locks the current UTC time.

End UTC

When the station finishes, check the box next to the end time.

This stamps and locks the current UTC time.

Manual Override

If a time needs correction, use the pencil edit option.

Times include seconds.

Example:

21:14:37Z

Manual entries can be typed in formats such as:

211437
21:14:37
2114
21:14
10. Compact Locked Time Display

When both UTC Start and UTC End are locked, the time controls collapse into a smaller read-only summary line.

This keeps the checklist clean.

To edit locked times, click the pencil icon.

11. Session-Level Clock

Next to the Current Session Checklist title, click the clock emoji.

This opens the session clock popup.

You can set:

Session Start UTC
Session End UTC

Unchecked times tick live.

Checking a box stamps and locks the current UTC time.

These times are saved and included in tactical reports.

12. Session Summary

Next to the session clock, click the notepad emoji.

This opens the Session Summary editor.

Use this to write a closing summary of the net.

Examples of summary content:

General net purpose
Number of check-ins
Notable traffic
Emergency or priority traffic
Frequency changes
Propagation conditions
Training notes
Closing remarks

When the session end time is checked, the tool prompts the net controller to complete a summary.

In Settings, the summary can be enabled or disabled for printing.

When enabled, the summary prints as its own final page in the tactical report.

13. RST, Weather, and Tactical Message

Each station card includes fields for:

RST

Default is usually 59.

Can be changed manually.

Weather

Use this for weather, location status, or station condition.

Examples:

Clear, 72F
Mobile
Battery power
Light rain
Tactical Message

Use this for message traffic or notes.

Examples:

Checked in with no traffic.
Has welfare traffic.
Relay from W3ABC.
Moved to 146.520 simplex.

Click Save Card to commit the card to the historical record.

14. Master Roster

The Master Roster stores all known stations.

It shows station details and history.

Operators may be color-coded by activity status.

The Master Roster is permanent unless wiped from Settings.

Do not use Wipe Database unless you intend to erase everything.

15. Manual Profile Editing

Click the pencil icon next to a station.

You can manually enter:

Name
License/profile type
Address or QTH
Latitude
Longitude

This is useful when:

QRZ is unavailable
Internet is down
The station is not found
Coordinates are missing
You need to plot someone on the map

Manual data stays saved until changed or overwritten by Full Database Sync.

16. QRZ Sync Modes
Sync New QRZ

The top button is intended for routine use.

It only looks up stations that have not already been QRZ synced.

This helps prevent bottlenecks.

FULL Database Sync

Located in Settings.

This attempts to refresh every station in the Master Roster.

Use it when:

You want to update old information
You want manual profiles refreshed from QRZ
You want to overwrite local entries with QRZ data

Full sync may take longer on large rosters.

17. Online and Offline Mode

The app includes an Online/Offline status button.

Online

The tool attempts QRZ lookups and online map tiles.

Offline

The tool avoids relying on QRZ and uses local cached information where possible.

New stations can still be manually entered.

18. Map Tab

Click the Map tab on the left side, or click the top map button if available.

The map shows stations with known coordinates.

Map Filters

You can filter by:

Current Session
Today’s Visitors
This Week
Last 30 Days
All Operators
NCO Marker

The Net Controller Station is shown as a large red dot.

Hover over it to see the net controller callsign.

Station Pins

Stations with latitude and longitude appear as pins.

Click or hover depending on the map mode to see station details.

Distance Lines

If enabled in Settings, lines are drawn from the NCO station to mapped stations.

Hovering over a line shows distance and bearing.

Offline Distance Grid

When offline, the map can use a distance grid.

The NCO is centered and stations plot by calculated distance and bearing from the NCO.

This is not a street map, but it remains useful without internet.

19. Printing the Map

From the Map tab, click Print Map.

This prints only the map.

It hides:

Header
Roster
Current Session
Settings
Tools
Sidebar controls

This is useful for a visual net coverage reference.

20. Propagation Tab

Click Propagation on the left side.

This displays HamQSL solar-terrestrial data.

This requires internet access.

Use it to quickly check propagation indicators and band condition references.

21. Tools Menu

Click the Tools dropdown in the top bar.

Script

Opens a saved editable script.

Use it for:

Net opening script
Net closing script
Emergency net script
Training net prompts
Club announcements

The script is saved locally.

Band Plan Map

Opens a zoomable band plan image.

Controls include:

Zoom in
Zoom out
Close popup

Use this as a quick frequency allocation reference.

22. ID Timer

The ID timer reminds the net controller to identify.

Open Settings to configure:

Enabled or disabled
Timer interval

When the timer expires, it alerts the operator.

After identifying, reset the timer.

23. Tactical PDF Report

Click Print Tactical PDF.

The report includes session and station details.

The report can include:

Net date
NCO location reference
Frequency
Mode
Session start and end time
Check-in order
Callsign
Operator details
Station address/QTH
Distance and bearing
Routine or emergency status
RST
Weather
Tactical message
Individual station start/end UTC
Optional session summary page

Use your browser’s print dialog to print or save as PDF.

24. Printing the Session Summary

Open Settings.

Enable the option to print the session summary.

When enabled, the session summary prints as its own final page in the tactical report.

25. Exporting Data

Open Settings.

Click Export Data.

This downloads a JSON backup of your database.

The export may include:

Master Roster
Current Session
Session frequency/mode
Session times
Session summaries
Historical station records
Saved settings where applicable

Export regularly if you want backups.

26. Importing Data

Open Settings.

Click Import Data.

Select a previously exported JSON file.

The tool will load the saved database.

Use this when moving to another computer or restoring a backup.

27. Clearing the Current Session

Click Clear Current Session.

This clears only the active checklist.

It does not delete the Master Roster.

Use this after a net is complete and you are ready to start fresh.

28. Wiping the Entire Database

Open Settings.

Use Wipe Entire Database only when you truly want to erase everything.

The tool requires strong confirmation.

This action removes the saved roster and historical data.

There is no undo unless you have an exported backup.

29. Recommended Net Workflow
Before the Net
Open the HTML file.
Confirm QRZ is authenticated if internet is available.
Confirm Net Controller Station is correct.
Set frequency and mode in Settings.
Open the session clock and start the session time.
Open your script from Tools if needed.
Confirm ID timer is enabled if desired.
During the Net
Type each callsign and press Enter.
Let QRZ populate the station when available.
Use cached or manual profile data when offline.
Track each station’s UTC start and end time.
Enter RST, weather, and tactical traffic.
Mark emergency traffic when applicable.
Rearrange station order if needed.
Use the map to view station distribution.
Save each card as needed.
At the End of the Net
Lock the session end UTC time.
Complete the session summary when prompted.
Save final station cards.
Print or save the tactical report as PDF.
Export a backup if desired.
Clear Current Session when ready for the next net.
30. Best Practices
Export your database regularly.
Do not wipe the database unless you have a backup.
Use manual profile editing for important stations with missing coordinates.
Set your NCO coordinates correctly for accurate distance and bearing.
Use Sync New QRZ during normal operations.
Use Full Database Sync only when you want a complete refresh.
Complete the session summary before printing the final report.
Save tactical cards before closing the browser.
Use the offline distance grid as a backup when internet is unavailable.
Short Promotional Version

Net Control Tool is a modern, single-file amateur radio net control dashboard built for fast check-ins, reliable local station records, live QRZ-assisted lookups, tactical message tracking, UTC timing, mapping, propagation monitoring, and professional PDF reporting.

It gives net controllers a clean command-center style interface with a permanent Master Roster, live Current Session Checklist, operator profile editor, emergency traffic marking, NCO station highlighting, station distance mapping, ID timer, session summary, band plan reference, net script tool, and printable tactical reports.

Designed for both casual ham radio nets and more structured emergency practice nets, it works online with QRZ and map tiles, but still remains useful offline through cached station data, manual profiles, and a distance-grid map.

All of this runs from one simple HTML file with no installer, no server, and no complicated setup.
