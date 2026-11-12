# Hosted pages for RadScan (the whole site, both apps)

The site is GitHub Pages, repo `sadkins0101/radscan`, served at https://sadkins0101.github.io/radscan/. **This folder
is the complete site**: `privacy.html`, `support.html`, `style.css` and the iOS images (`img/iphone-*.webp`,
`ipad-console.webp`, `waterfall-wide.webp`, the icons, `og.jpg`) are copies from the iOS repo (`../ios/docs/site`) as
of iOS commit `d49fac9`; copy them again when they change there.

- https://sadkins0101.github.io/radscan/ shows iPhone and iPad (on an Android device, or after choosing Android
  there before, it shows Android).
- https://sadkins0101.github.io/radscan/?android always shows Android; `?ios` always shows iPhone and iPad.

## What's here, and where it goes

Upload everything in this folder (except this README) to the root of the Pages repo, keeping the names:

- `index.html`: **the front page for both apps; it replaces the iOS-only one.** It shows iPhone and iPad unless
  Android is chosen: by the switch in its bar, by `?android` in the address, by the choice made there before, or by
  opening it on an Android device. Everything marked `class="only-ios"` or `class="only-android"` shows for that app
  only; a link with `data-android="…"` goes to the Android page when Android is chosen.
  **The address to give in the Play Console (Website) is https://sadkins0101.github.io/radscan/?android .**
- `img/android-*.webp`: the Android screenshots (Virtual Scanner, emulator, dark theme): seven phone screens at
  780 × 1751, `android-tablet-console.webp` and `android-waterfall-wide.webp`. They go in the site's `img/` beside
  the iOS ones. The icon, favicon and `og.jpg` are shared.
- `privacy-android.html`, `support-android.html`: what the Android app's Settings › Privacy Policy and Support rows
  open (`AppInfo.kt`), and the Play Console's privacy policy address. They are the iOS pages with Android's facts
  (FTP passwords under an Android Keystore key, OpenStreetMap tiles, the device's geocoder, Google Play, location
  read only on Move Scanner Here) and use the site's `style.css`. Until they are uploaded the two rows open "not found".

The support and contact address everywhere is **radscan@enetworx.net** (iOS changelog 0075); use it for the Play
listing's developer email too.

## Keeping `index.html` in step with iOS

`index.html` was made from the iOS repo's `docs/site/index.html` as of iOS commit `d49fac9` (0077), with the Android
parts added beside the iOS ones. **The iOS repo's copy is still the iOS-only page**: if it is uploaded again it
replaces this one and the Android half disappears. Either copy this file into the iOS repo, or make later edits to
the front page here. When the stores go live, the `data-store="ios"` and `data-store="android"` buttons become the
store links (see the comment at the top of the file).

To look at it locally: `python3 -m http.server 8765` in this folder, then open http://localhost:8765/ and
http://localhost:8765/?android .
