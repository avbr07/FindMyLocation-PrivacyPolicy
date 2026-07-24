# Privacy Policy for Find My Location

**Last updated:** July 24, 2026  
**Developer:** PlayMine  
**Package:** net.playmine.findmylocation

## Overview
Find My Location ("the App") is a utility that shows your current location, address, weather, travel speed, altitude/flight height, and steps — and keeps a short, on-device-only log of your recent trips so you can view your travelled routes. We are committed to protecting your privacy.

## Data Collection
The App does **NOT** collect, store, or transmit any personal data to servers operated by us. We do not use analytics, tracking, or advertising SDKs that collect personal information. We do not require an account, sign-in, or any personal details. The App counts fully **anonymous usage statistics** (only how many times the app is opened — never your location, routes, or anything that could identify you or your device); see the "Anonymous Usage Statistics" section below, including how to turn this off.

## Location Data
- Your location is determined on-device using Google Play Services (GPS/network).
- To convert coordinates into a human-readable address (reverse geocoding), the App first uses your device's **built-in geocoder** (provided by Google Play services on most devices); if it cannot resolve a street-level address, coordinates are sent to **Nominatim (OpenStreetMap)** instead. In both cases only the coordinates are shared, solely for this purpose.
- Location coordinates are sent to **OpenWeatherMap** and/or **Open-Meteo** solely to fetch current weather conditions.
- Location coordinates are sent to **Open-Meteo** solely to look up terrain ground elevation, used to calculate height above ground ("flight height").
- When you view the map, your approximate location (as map-tile coordinates) is sent to the **OpenStreetMap tile servers** to display map imagery.
- If you tap the Map tab's **fuel (Petrol/Gas)**, **Food** or **Attractions** buttons, your coordinates and chosen search radius are sent to the **Overpass API** (an OpenStreetMap community service) to find nearby fuel stations, restaurants and attractions. For **Attractions**, your coordinates are **also** sent to the **Wikidata Query Service (Wikimedia)** to find famous/notable places nearby (temples, monuments, museums and the like). This happens only when you use those buttons.
- If you **tap a place on the map**, the App reverse-geocodes that point (built-in geocoder first, then Nominatim if needed — as above) to show its address; only the tapped coordinates are shared, solely for this purpose.
- If you type a place into the Map tab's **search box** (a ZIP code, city and state, landmark or address), that text is sent to your device's **built-in geocoder** and, if it finds nothing, to **Nominatim (OpenStreetMap)**, solely to turn it into a point on the map. Your approximate location is sent with it only so that nearby matches are ranked first. This happens only when you run a search; the text you type is not stored by the App or sent anywhere else.
- Speed, trip distance, and altitude are derived on-device from the GPS signal and are not transmitted anywhere.
- The compass heading is derived on-device from the phone's motion (magnetometer) sensors. It is never transmitted.
- Step counts (and the calorie/distance estimates derived from them) come from your phone's step sensor and accelerometer, are computed on-device, and are never transmitted.
- **Trip history stays on your device.** To power the Trips tab, the App keeps a log of your recent journeys (coordinates, place names, and times) **in the App's private storage on your device only**, for your **7 most recent travel days, and never longer than 30 days**: a day's trips are deleted automatically once 7 newer days with travel have been recorded (days you don't travel don't shorten this), and any trip **older than 30 days is deleted regardless**. This history is **never transmitted** to us or to any third party (viewing a route on the map only fetches map imagery, as above), and it is removed entirely if you uninstall the App. All other location data is held in memory only during active use and is discarded when tracking stops or the app is closed.

## Background Location
- The App offers two **optional**, separately controlled features that use location while the screen is locked or the app is in the background. Both are off until you turn them on, both run as an Android **foreground service** with an **ongoing, visible notification** so you always know when they are active, and both can be stopped at any time:
  - **Keep running in background** — keeps updating and announcing your location continuously until you switch it off.
  - **Trip recording** — saves your walks and drives to the on-device Trips tab, tracing each journey's route even while the phone is locked or in your pocket. The screen-locked part runs **only while a trip is being recorded** and only after you have confirmed it (a one-time prompt on your first trip, or by turning the Trip recording switch on yourself); it stops itself when the journey ends and does not announce or geocode anything. One switch controls all trip recording — in Settings, at the top of the Trips tab, or by long-pressing the Trips tab — and switching it off stops all trip recording and its GPS use entirely.
- Background location is used **only** to provide the App's core features you enabled — live location, address, voice announcements, and on-device trip recording (routes, speed and distance). It is **never** used for advertising, profiling, or shared with third parties beyond the reverse-geocoding and weather services listed below, which receive only coordinates. Trip routes recorded in the background stay in the same on-device trip history described above (your 7 most recent travel days, nothing older than 30 days) and are never transmitted.
- Background location updates occur only while one of these features is enabled, and stop when it stops.

## Voice Announcements
- The App can read your current place name aloud using your device's built-in **on-device text-to-speech** engine.
- No audio, and no location text, is sent off the device for this feature.

## Anonymous Usage Statistics
To understand how many people use the App, the App counts exactly two usage events using **Aptabase**, a privacy-first analytics service, hosted in the **European Union (Germany)**:

- **What is counted:** the app's very first launch after being installed, and the app being opened. Nothing else — no tabs, no trips, no settings, and **never the routes, places, or any coordinates**. Each event carries only basic app/device context: app version, Android version, device model, and the country/locale reported by the system.
- **What is never sent:** no device ID, advertising ID, hardware identifier, account identifier, name, email, precise location, addresses, place names, or trip routes. There is nothing in the data that can identify you or your device.
- **How anonymity works:** Aptabase does not use identifiers. Sessions are grouped using a hash of the network address and user agent combined with a **salt that rotates every day**, so activity cannot be linked to any individual and cannot be correlated across days. Raw IP addresses are not stored.
- **Your control:** you can turn this off at any time in **Settings → Privacy → Share anonymous usage statistics**. When off, nothing is sent.
- **Retention:** the anonymous, aggregate event counts are retained by Aptabase for up to 5 years (see https://aptabase.com/legal/privacy). Because the data is anonymous by design, it cannot be traced back to you, and there is nothing personal in it to delete.

## Third-Party Services
| Service | Purpose | Data Sent | Privacy Policy |
|---------|---------|-----------|---------------|
| Google Play Services | GPS / network location | None (on-device) | https://policies.google.com/privacy |
| Device geocoder (Google Play services) | Reverse geocoding (address) — primary; place search — primary (only when you use the Map search box) | Lat/Lon coordinates; the place text you type | https://policies.google.com/privacy |
| Nominatim (OpenStreetMap) | Reverse geocoding (address) — fallback; place search — fallback (only when you use the Map search box) | Lat/Lon coordinates, IP; the place text you type | https://osmfoundation.org/wiki/Privacy_Policy |
| OpenStreetMap tile servers | Map display | Approximate location (tile coords), IP | https://osmfoundation.org/wiki/Privacy_Policy |
| Overpass API (OpenStreetMap community) | Nearby fuel stations, restaurants & attractions (only when you tap Petrol/Gas, Food or Attractions) | Lat/Lon coordinates + search radius, IP | https://osmfoundation.org/wiki/Privacy_Policy |
| Wikidata Query Service (Wikimedia) | Famous/notable attractions near a point (only when you use the Attractions button) | Lat/Lon coordinates, IP | https://foundation.wikimedia.org/wiki/Policy:Privacy_policy |
| OpenWeatherMap | Weather data | Lat/Lon coordinates, IP | https://openweather.co.uk/privacy-policy |
| Open-Meteo | Weather and ground-elevation data | Lat/Lon coordinates, IP | https://open-meteo.com/en/terms |
| Google Play In-App Updates | App updates | None (system-level) | https://policies.google.com/privacy |
| Google Play In-App Review | User ratings | None (system-level) | https://policies.google.com/privacy |
| Aptabase (EU-hosted) | Anonymous usage statistics | Anonymous event counts + app version, Android version, device model, country/locale — **no identifiers, no location** | https://aptabase.com/legal/privacy |

When you tap **Share**, the App builds a Google Maps link with your coordinates and hands it to whichever app you choose to share with. Nothing is shared until you select a destination.

## Advertising
The current version of the App does **not** display advertisements. Future versions may include ads served by Google AdMob. If ads are introduced, this privacy policy will be updated accordingly, and AdMob's data practices will apply (https://policies.google.com/technologies/ads).

## Permissions
| Permission | Purpose |
|-----------|---------|
| ACCESS_FINE_LOCATION | Determine precise GPS position for location, speed, and altitude |
| ACCESS_COARSE_LOCATION | Fallback network-based location |
| INTERNET | Fetch address, weather, elevation, and map data |
| FOREGROUND_SERVICE | Run optional background location tracking |
| FOREGROUND_SERVICE_LOCATION | Declare the background service as a location service (Android 14+) |
| POST_NOTIFICATIONS | Show the ongoing tracking notification (Android 13+) |
| ACTIVITY_RECOGNITION | Count steps for the Speed tab's step counter, and — while trip recording is on — notice when you start moving so a trip can begin even if the phone was locked before you left (optional — Android 10+; denying it only disables step counting and this automatic start) |
| ACCESS_NETWORK_STATE | Let the map check for connectivity before fetching tiles |
| RECEIVE_BOOT_COMPLETED | Re-enable that automatic trip start after the phone restarts, if trip recording is on |

## Data Storage
- The only location data written to storage is the **on-device trip history** described above: kept in the App's private storage, auto-deleted past your 7 most recent travel days (and always past 30 days of age), never transmitted, and removed on uninstall.
- The App also stores non-personal app preferences on-device: a days-of-use counter (for the review prompt), the voice-announcement on/off setting, the in-app voice volume level, the keep-screen-awake setting, the preferred speed unit (mph/km/h), the preferred temperature unit (°F/°C), your daily step count, the anonymous-usage-statistics on/off setting, and a counter of postponed app-update reminders.
- If you choose to enter your body weight (used only to estimate calories from your steps), it is stored on-device only and never leaves your phone.
- No personal information is collected by us.

## Data Retention
We operate no servers and retain **no user data of any kind** on our side. All data the App uses lives only on your device, with these retention periods:

| Data | Where it is kept | How long |
|------|------------------|----------|
| Trip history (routes, place names, times) | App's private on-device storage | Your **7 most recent travel days, at most 30 days old** — a day's trips are deleted once 7 newer travel days exist, and anything older than 30 days is deleted regardless |
| Current location, address, weather, speed, altitude, compass | Device memory only | Discarded when tracking stops or the App closes |
| App preferences (units, voice settings, optional body weight, step count, usage counters) | App's private on-device storage | Until you delete them or uninstall the App |
| Anonymous usage statistics (event counts — no identifiers, no location) | Aptabase (EU) | Up to 5 years, in anonymous aggregate form only |

The third-party services listed above (geocoding, weather, elevation, map tiles) receive coordinates transiently to answer each request; we do not control their retention, which is governed by their own privacy policies linked in the table above.

## Data Deletion
Because we never collect or store your data on any server, **there is no data for us to delete** — everything is on your device and under your control. You can delete it at any time:

- **Delete everything instantly:** uninstall the App, or go to **Android Settings → Apps → Find My Location → Storage → Clear data**. This permanently removes the trip history, all preferences, and any stored weight — nothing survives anywhere else.
- **Trip history** also prunes itself automatically: only your 7 most recent travel days are kept, and nothing older than 30 days.
- **Anonymous usage statistics** contain no identifiers by design, so they cannot be traced back to you or your device — there is nothing personal in them to delete. You can stop them being counted at any time in **Settings → Privacy**.

If you have any questions or requests regarding your data, contact us at **playmine.support@gmail.com** and we will respond promptly.

## Data Sharing
We do not sell, trade, or share your data with any third party beyond the services described above, each of which receives only the coordinates needed to perform its function.

## Data Security & Handling
We handle the personal and sensitive data the App works with (your location) as follows:

- Location is processed **on your device**. The only data written to disk — the trip history (your 7 most recent travel days, nothing older than 30 days) and your preferences — is stored in the App's **private, sandboxed storage**, which Android prevents other apps from reading.
- All network communications (geocoding, weather, elevation, map tiles) use **HTTPS/TLS encryption** and carry only coordinates — never your name, contacts, identifiers, or anything else, because the App never has such information.
- No personal data is ever transmitted to servers operated by us; we have no servers and no user database.

## Children's Privacy
The App does not knowingly collect data from children under 13. The App does not require account creation or personal information.

## Changes to This Policy
We may update this privacy policy from time to time. Changes will be reflected in the "Last updated" date above. Continued use of the App constitutes acceptance of the updated policy.

## Contact
If you have questions about this privacy policy, contact us at:  
📧 playmine.support@gmail.com

## Consent
By using Find My Location, you consent to this privacy policy.
