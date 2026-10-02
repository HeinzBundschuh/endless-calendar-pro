# Endless Calendar Pro

A complete calendar in **one single HTML file**. No installation, no account, no server: open the file in a browser and it works – offline, on Windows, Linux, macOS and Android. Your events stay in your browser.

🇩🇪 [Deutsche Version](README.de.md)

![Month view](docs/screenshots/monat.png)

The user interface is in German. The German terms you will see are given in brackets below.

## Use it

1. Download `endless_calendar_pro_V3_1.html` from the [releases](../../releases) (or from this repository).
2. Open it in a browser (Firefox, Chrome, Edge …). That's all.

Events are stored in the browser's local storage for this file. Use **ICS ↕ → JSON Backup** regularly to save a backup file; it is also the way to move your calendar to another browser or device. The info bar reminds you when the last backup is some time ago.

## Overview

- Five views: year, month, week, day, list
- Mouse operation: drag, copy, merge, right-click menu
- Recurring events with many rules, and exceptions for single occurrences
- Categories with colour and emoji, birthdays and memorial days
- Austrian holidays and special days
- Search, hide and show, conflict warning
- Undo, restore points, ICS and JSON import/export, duplicate clean-up
- Dark mode, full screen, desktop and mobile layout

## Views and navigation

- **Year** (*Jahr*): twelve months with week numbers; days with events are marked.
- **Month** (*Monat*): grid with event chips and the month's event list below. If a day is full, "+N mehr" opens the day view.
- **Week** (*Woche*) and **day** (*Tag*): events with times; events running past midnight show their start date on the following days.
- **List** (*Liste*): all events of a year; multi-day events as one entry with its date range.
- **Sidebar:** mini calendar and "Demnächst" (coming up) with the next occurrence of each event.
- **Info bar:** today's date, week number, day of the year, today's events.
- **Flipping:** arrows ◀ ▶, the **Heute** (today) button, mouse wheel over the calendar (months, years, weeks, days), swiping on a touch screen.

![Year view](docs/screenshots/jahr.png)

## Mouse operation

**Drag and drop (month view)**

| Action | Effect |
|---|---|
| Drag an event to another day | moves the event |
| Drag with **Ctrl** or **Shift** | copies the event, the original stays |
| Drop an event onto another event | merges both into one (titles joined with "+", notes kept) |

For recurring events, dragging affects only the occurrence you grabbed. If the result overlaps another event, the confirmation shows a warning – with **Undo** right next to it.

**Right-click an event** (month, week, day, list, "Demnächst")

- 📄 Copy (*Termin kopieren*)
- ✏️ Edit (*Bearbeiten*)
- ↔ Move to a target date (*Verschieben*; for a series only this occurrence)
- 📍 Jump to the event (*Springe zu Termin*; opens the day view)
- 🙈 Hide the event or its whole category (*ausblenden*)
- 🗑 Delete (*Löschen*)

**Right-click a day**

- 📋 New event (*Neuer Termin*)
- 📅 Show the day (*Tag ansehen*)
- 📥 Paste the copied event (*Einfügen*) – as often as you like, also in other months

On a phone, a long press replaces the right-click.

## Events

- Title, category, date, time from–to, notes.
- **Multi-day** via an end date; **past midnight** (e.g. 22:00–01:00) with a confirmation when saving.
- **Reminder:** 1, 2 or 3 days or 1 week before. With the bell 🔔 switched on, reminders appear as browser notifications while the page is open.
- **Colour per event:** the category colour, one of eight pastel colours or a custom colour; optionally a custom text colour. Otherwise the text colour is chosen automatically for contrast.
- **Display per event** in the month view: with colour background, coloured border only, or text only.
- **Event type:** event, holiday, private event, or hidden event (visible in the list only).
- **Input checks:** end before start, end time without start time and similar mistakes are caught when saving.
- **Conflict warning ⚠️:** overlaps are shown when saving and in the day view, also for series and multi-day events.

## Recurring events

- **Simple:** weekly, monthly, yearly.
- **Free interval:** every *n* hours, days, weeks, months or years; for hours also as `HH:MM` (e.g. every 02:30 hours).
- **Weekday in a month:** e.g. "first Monday in May" or "last Friday of every month".
- **Movable dates:** relative to Easter or to the first Sunday of Advent.
- **Extra conditions:** tick boxes for weekdays and months, e.g. "Friday the 13th" or "weekdays in summer only".
- **End:** never, after *n* occurrences, or on a date; optionally skip holidays.
- **Exceptions:** delete or move a single occurrence without changing the series.
- Yearly events show the years since their start in brackets (birthday: age, wedding day: years).

## Categories

- Five categories are predefined: event, birthday, holiday, private event, other.
- Under **Kategorien** you create your own and change name, colour and emoji.
- New events take the colour of their category and follow later colour changes.
- Each category can be **hidden and shown** with a switch.
- New events in birthday, memorial and anniversary categories start with a yearly repeat.

## Birthdays and memorial days

- Birthdays show the age: "Anna (41)".
- With an optional date of death, the birthday continues as "Name (would have turned 94)", and a yearly memorial day "✝ Name (13)" appears on the date of death.
- Birthdays can be imported from a `birthday.dat` file (Ewiger Kalender).

## Holidays and special days

Austrian public holidays and special days are calculated for every year, including the days that depend on Easter (Maundy Thursday to Pentecost), Advent, clock changes, Shrove Tuesday, St. Martin's Day and Christmas Eve. They appear in one consistent colour and are found by the search.

## Search

The magnifier 🔍 searches titles, notes and categories of all events. It also finds holidays and special days (current year ± 2 years). Every hit has a **Springe zu Termin** (jump to event) button.

## Hide and show

- Single events or whole categories can be hidden. This is display only: data, backups and reminders stay unchanged.
- In the event list below the month view and in the list view, hidden events stay visible in a dimmed style and can be shown again with 👁.
- A notice bar shows what is hidden, with the button **Alles einblenden** (show everything).

## Undo and safety

- **Undo:** the last 30 changes, with the **↩ Rückgängig** button in the header or **Ctrl+Z**. The tooltip names the action that will be undone.
- **Restore point:** before every import and before the duplicate clean-up the current state is saved; restore it under **ICS ↕ → Wartung** (maintenance).
- **Deleting:** the buttons say exactly what is deleted ("this occurrence only", "series", "whole period"). The confirmation names the event, the scope and the period.
- **Skip the delete confirmation:** the settings ⚙ offer "Beim Löschen einzelner Termine nicht nachfragen" (do not ask when deleting single events). Series and periods still ask, to be safe; undo is always possible.
- **Several tabs:** changes made in another tab are detected; undo is then blocked instead of overwriting the other tab's data.

## Import, export and maintenance (the "ICS ↕" button)

- **ICS export** as a file or as text, standards-compliant for Google Calendar, Outlook, Thunderbird and others.
- **ICS import with preview:** the file is only read and checked first. You see what is new, duplicate or faulty, select what you want, and only then import.
- Import of **birthday.dat**.
- **JSON backup** as a file or as text. When loading you choose **Zusammenführen** (merge, recommended) or **Ersetzen** (replace).
- **Maintenance – remove duplicates** (*Duplikate entfernen*): finds exact duplicates, similar pairs (same name and date) and identical series with different start dates. A preview shows every planned change before anything is removed; cancelling leaves everything untouched.
- **Maintenance – restore the restore point** (*Sicherungspunkt wiederherstellen*).

## Settings and appearance (⚙)

- **Light** or **dark**, with a selectable accent colour (presets or any colour).
- Event chips with colour background, with coloured border, or both.
- Delete confirmation for single events on or off.
- **Full screen** with the ⛶ button in the header.

## Desktop and mobile

| | Desktop | Phone and tablet |
|---|---|---|
| Menu | right-click | long press |
| Flipping | mouse wheel, arrows | swipe, arrows |
| Moving | drag and drop | menu "↔ Verschieben" |
| Keyboard | Ctrl+Z, Esc closes dialogs | – |
| Layout | sidebar next to the calendar | single column, compact header |

Tip for Android: choose "Add to Home screen" in the browser menu. Together with the full-screen button the calendar then starts like an app.

## How it works

Everything – HTML, CSS and JavaScript – is in one file without external libraries or network requests. The version history is documented at the top of the file.

Data is kept in `localStorage` (key `ecpro_v1`). It belongs to the browser profile and the place the file is opened from; clearing the browser data deletes it, so keep backups.

## Contributing

Bug reports and ideas are welcome – please open an [issue](../../issues).

## Privacy

The file sends no data anywhere. There is no tracking, no analytics and no advertising.

## Licence

[MIT](LICENSE) © 2026 Heinz Bundschuh
