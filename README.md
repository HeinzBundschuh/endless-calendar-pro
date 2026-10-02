# Endless Calendar Pro

A complete calendar in **one single HTML file**. No installation, no account, no server: open the file in a browser and it works – offline, on Windows, Linux, macOS and Android. Your events stay in your browser.

🇩🇪 [Deutsche Version](README.de.md)

![Month view](docs/screenshots/monat.png)

The user interface is in German.

## Use it

1. Download `endless_calendar_pro_V3_1.html` from the [releases](../../releases) (or from this repository).
2. Open it in a browser (Firefox, Chrome, Edge …). That's all.

Events are stored in the browser's local storage for this file. Use **ICS ↕ → JSON Backup** regularly to save a backup file; it is also the way to move your calendar to another browser or device.

## Features

- **Five views:** year, month, week, day and list; mini calendar and "coming up" list in the sidebar; ISO week numbers and day of the year.
- **Categories** with colour and emoji; per-event colour, text colour and display style.
- **Recurring events:** daily to yearly, free intervals ("every 3 weeks"), "first Monday in May", weekday and month masks ("Friday the 13th", "summer only"), end date or number of occurrences, skip holidays, exceptions for single occurrences (move or delete one).
- **Birthdays** with age, and memorial days for deceased contacts.
- **Austrian holidays** and special days, calculated for every year (Easter-based days, clock change …).
- Multi-day and past-midnight events, drag and drop, copy and paste, conflict warning.
- **Search** across all events; hide and show single events or whole series.
- **Undo** and persistent restore points before risky actions.
- **Import/export:** ICS (standards-compliant), JSON backup with merge or replace, duplicate clean-up, import of `birthday.dat`.
- Reminders as browser notifications while the page is open.
- Dark mode with selectable accent colour, full-screen mode, mobile layout with swipe navigation.

![Year view](docs/screenshots/jahr.png)

## How it works

Everything – HTML, CSS and JavaScript – is in one file without external libraries or network requests. The version history is documented at the top of the file.

Data is kept in `localStorage` (key `ecpro_v1`). It belongs to the browser profile and the place the file is opened from; clearing the browser data deletes it, so keep backups.

## Contributing

Bug reports and ideas are welcome – please open an [issue](../../issues).

## Privacy

The file sends no data anywhere. There is no tracking, no analytics and no advertising.

## Licence

[MIT](LICENSE) © 2026 Heinz Bundschuh
