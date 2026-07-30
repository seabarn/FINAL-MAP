# FINAL-MAP — How to Update the Map

The website displays the map from this file:

```
HMH-FFFF.kml
```

The website links to that **exact filename**. To update the map, you replace this file with a new export from Google My Maps — **keeping the same name**. Do not rename it, and do not upload extra copies with new names (e.g. `HMH-FFFF-2026.kml`), or the website will keep showing the old map.

> **Don't worry about losing the old version.** GitHub automatically keeps a full history of every change. If an update goes wrong, any previous version can be restored (see "Restoring an old version" below).

---

## Step 1 — Update the map in Google My Maps

1. Open the map in [Google My Maps](https://www.google.com/maps/d/).
2. Make your edits (move pins, edit areas, add photos, etc.).
3. Changes save automatically.

**If your placemarks have photos:** click a pin and check the photo actually appears in its popup before exporting. Photos that aren't attached to the pin will not be included in the export.

## Step 2 — Export the map as KML

1. In My Maps, click the **⋮** (three dots) next to the map title.
2. Choose **Export to KML/KMZ**.
3. In the dropdown, select the **entire map** (not a single layer).
4. **Tick the box "Export as KML instead of KMZ"** — the website needs `.kml`, not `.kmz`.
5. Click **Download**.

The downloaded file will be named after the map (e.g. `HMH.kml`) — that's expected; we rename it next.

## Step 3 — Rename the downloaded file

Rename the downloaded file to exactly:

```
HMH-FFFF.kml
```

Spelling, capitalisation, and the `.kml` extension must all match exactly.

## Step 4 — Upload to GitHub (replaces the old file)

1. Go to the repository: <https://github.com/seabarn/FINAL-MAP>
2. Click **Add file → Upload files** (top right of the file list).
3. Drag in your renamed `HMH-FFFF.kml`.
4. In the commit message box, write a short note, e.g. `Update map – July 2026`.
5. Click **Commit changes**.

Because the filename matches, GitHub **replaces** the old file with the new one. The website link doesn't change and doesn't break.

## Step 5 — Check it worked

1. Open <https://github.com/seabarn/FINAL-MAP/blob/main/HMH-FFFF.kml> and confirm the "last commit" date at the top is today.
2. Check the website. **Allow up to 5–10 minutes** — GitHub caches files briefly, so the site may show the old map for a few minutes after upload.

**If the map should include photos:** open the file on GitHub (link above) and use your browser's find (Ctrl/Cmd-F) to search for `gx_media_links`. If it's not found, the export contains no photos — go back to Step 1 and check the photos are attached to the pins in My Maps, then export again.

---

## Restoring an old version

If an update breaks something:

1. Go to the file on GitHub and click **History** (top right).
2. Click the version you want to go back to.
3. Click **⋯ → View file**, then **Download raw file**.
4. Rename it to `HMH-FFFF.kml` if needed and re-upload it (Step 4 above).

---

## FAQ

**Why not name the files by date/year?**
The website points at one fixed URL containing the filename. A new filename means a new URL the website doesn't know about. GitHub's built-in history already records when each change happened and what it contained, so dated filenames add nothing — they just cause broken links.

**KML or KMZ?**
Always KML. The website reads `HMH-FFFF.kml`; a `.kmz` upload would sit alongside it unused.

**What about the photos on the pins?**
Photos are not embedded in the KML file — the export contains links to images hosted on Google's servers. Two things follow: (1) the photos must be attached to pins in My Maps *at the time of export*, and (2) if the My Maps map is ever deleted, the photo links in the KML will stop working even though the KML itself is fine.
