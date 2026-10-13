# Antenna Check Template

A single-file HTML tool for checking the satellite antennas on a ship. It shows a top-view plan of the ship, lets you mark each antenna's status, attach notes and photos, and produces a PDF report. It works offline and needs no installation.

## Quick start

1. Download `antenna-status.html`.
2. Open it in a modern browser on your phone or computer.
3. Tap an antenna to set its status, add a note or attach photos.

There is no server, account or internet connection involved.

## The plan view

- The ship is shown from above with the **bow at the top**. A circled **H** at the tip marks the helipad for orientation.
- Antennas are grouped into **locations** (by default FWD, MID and AFT). Each location's tag and name appear beside the hull, level with its antennas.
- Antennas are arranged two per row.
- **Starlink** antennas are square. **Kymeta OneWeb** antennas are rounded squares.
- Locations with no antennas are not shown on the map.

### Default layout

| Location | Name | Antennas |
|----------|------|----------|
| FWD | Solarium | KY-2, SL-8 |
| MID | Lawn Club | KY-1, SL-7, SL-5, SL-6, SL-3, SL-4, SL-1, SL-2 |
| AFT | Stern | none yet (shown as open deck space) |

Names and positions can all be changed in settings.

## Checking an antenna

Tap an antenna to open its panel at the bottom of the screen.

- **Status:** Unchecked, OK, Issue or Down. The counters at the top of the page update straight away.
- **Name:** rename the antenna.
- **Note:** free text, for example "no lock" or "cable damaged". A small dot on the antenna shows it has a note.
- **Photos:** tap **Add photo** to take a picture or choose one from your gallery. You can attach several. Tap a thumbnail to open the photo full screen, then tap the photo to zoom in and out. Use **Delete** (tap twice to confirm) to remove a photo.

## Settings

Tap the gear icon in the top right to edit the layout.

- Rename a location's tag (for example FWD, MID, AFT) and its name.
- Add an antenna to a location by choosing a type (Starlink, Kymeta OneWeb or Other). New antennas get the next free number, such as SL-9 or KY-3.
- Rename, change the type of, move up or down, or remove any antenna.
- Add, reorder or remove whole locations.

Removing an antenna or a location needs a second tap to confirm, and permanently deletes its status, note and photos.

## PDF report

Tap **Generate PDF report**. The browser's print dialog opens. Choose **Save as PDF** as the destination.

The report contains:

- The date and time, and counts of Unchecked, OK, Issue and Down antennas.
- A colour-coded plan of the antennas by location.
- A table with every antenna's type, location, status, last update, note and number of photos.
- All photos, grouped by antenna.

The suggested file name includes the date and time.

## Where your data is stored

Everything is stored in the browser on the device you are using:

- Statuses, notes and the layout are kept in the browser's local storage.
- Photos are resized to a smaller JPEG and kept in the browser's IndexedDB.

This means:

- Data is **not synced** between devices or browsers.
- Clearing the browser's site data deletes it.
- Opening the file from a different location or in a different browser starts with a fresh copy.
- Some private or incognito windows cannot store photos. The page warns you if this is the case.

Generate the PDF report on the same device where you recorded the checks.

**Reset all** clears every status, note and photo. It does not change the layout.

## Notes

- The page follows your device's light or dark setting.
- Fonts fall back to your device's built-in fonts when you are offline, so the lettering may look slightly different.
- The PDF report lists the locations in plan order but does not include the ship outline.

## Files

| File | Purpose |
|------|---------|
| `antenna-status.html` | The whole application: page, styles and script in one file |
| `README.md` | This file |
