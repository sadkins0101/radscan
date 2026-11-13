# Hosted pages for RadScan (the whole site, both apps)

The site is GitHub Pages, repo `sadkins0101/radscan`, served at https://radscan.enetworx.net/ (the owner's domain, at
Hover: `CNAME radscan → sadkins0101.github.io`; the `CNAME` file here tells GitHub Pages the domain and must stay in
the repo's root; the old https://sadkins0101.github.io/radscan/ addresses redirect to it). **This folder
is the complete site and the authority for both apps** (the owner's call, 2026-11-12): every page change, iOS or
Android, is made here and uploaded from here. The iOS repo's `docs/site` (`../ios/docs/site`) is a copy taken at
Android commit `5c8c7fb` (iOS changelog 0078); it had nothing this folder lacks when compared on 2026-11-12.
Changed here since that copy, for the iOS side to take when it next copies: `index.html` (the addresses now
radscan.enetworx.net) and the new `CNAME` file. The site may move to a repo of its own later.

- https://radscan.enetworx.net/ shows iPhone and iPad (on an Android device, or after choosing Android
  there before, it shows Android).
- https://radscan.enetworx.net/?android always shows Android; `?ios` always shows iPhone and iPad.

## What's here, and where it goes

Upload everything in this folder (except this README) to the root of the Pages repo, keeping the names:

- `index.html`: **the front page for both apps; it replaces the iOS-only one.** It shows iPhone and iPad unless
  Android is chosen: by the switch in its bar, by `?android` in the address, by the choice made there before, or by
  opening it on an Android device. Everything marked `class="only-ios"` or `class="only-android"` shows for that app
  only; a link with `data-android="…"` goes to the Android page when Android is chosen.
  **The address to give in the Play Console (Website) is https://radscan.enetworx.net/?android .**
- `img/android-*.webp`: the Android screenshots (Virtual Scanner, emulator, dark theme): seven phone screens at
  780 × 1751, `android-tablet-console.webp` and `android-waterfall-wide.webp`. They go in the site's `img/` beside
  the iOS ones. The icon, favicon and `og.jpg` are shared.
- `privacy-android.html`, `support-android.html`: what the Android app's Settings › Privacy Policy and Support rows
  open (`AppInfo.kt`), and the Play Console's privacy policy address. They are the iOS pages with Android's facts
  (FTP passwords under an Android Keystore key, OpenStreetMap tiles, the device's geocoder, Google Play, location
  read only on Move Scanner Here) and use the site's `style.css`. Until they are uploaded the two rows open "not found".

The support and contact address everywhere is **radscan@enetworx.net** (iOS changelog 0075); use it for the Play
listing's developer email too.

## Store links

When the stores go live, the `data-store="ios"` and `data-store="android"` buttons in `index.html` become the store
links (see the `STORE LINKS` comment at the top of the file; the iOS one gets Apple's official badge, unaltered).

To look at it locally: `python3 -m http.server 8765` in this folder, then open http://localhost:8765/ and
http://localhost:8765/?android .
