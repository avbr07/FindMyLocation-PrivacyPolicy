# Privacy Policy for Find My Location

**Last updated:** August 31, 2026  
**Developer:** PlayMine  
**Package:** net.playmine.findmylocation

## Overview
Find My Location ("the App") is a utility that shows your current location, address, weather, travel speed, altitude/flight height, and steps — and keeps a short, on-device-only log of your recent trips so you can view your travelled routes. We are committed to protecting your privacy.

## Data Collection
The App does **NOT** collect, store, or transmit any personal data to servers operated by us. We do not use analytics, tracking, or advertising SDKs that collect personal information. We do not require an account, sign-in, or any personal details. The App counts fully **anonymous usage statistics** (only how many times the app is opened — never your location, routes, or anything that could identify you or your device); see the "Anonymous Usage Statistics" section below, including how to turn this off.

## Location Data
- Your location is determined on-device using Google Play Services (GPS/network).
- **Turning your coordinates into a place name no longer sends them anywhere.** The App carries a list of the world's towns and cities (**GeoNames**, CC BY 4.0) inside the app itself, so your city, region and country are worked out entirely on your device, with no connection and no request to anyone. This replaces the previous fallback to **Nominatim (OpenStreetMap)**, which has been **removed from the App entirely** for this purpose.
- For a full **street address**, the App uses your device's **built-in geocoder** (provided by Google Play services on most devices), which receives only the coordinates. If it cannot answer — including when you have no connection — the on-device list above supplies the place name instead.
- **Addresses the App has already looked up are remembered on your device** so the same street does not have to be looked up twice. This "place cache" holds the coordinates and address text for places you have been, in the App's private storage, capped at 15,000 entries, and each entry is deleted automatically after 14 days. It is never transmitted, and it is removed if you uninstall the App or clear its data.
- Location coordinates are sent to **OpenWeatherMap** and/or **Open-Meteo** solely to fetch current weather conditions. This happens **only while the App is open on screen**, at most once every 15 minutes, and only while you are near the place the displayed reading came from — plus whenever you tap the weather card's refresh or **Show** button. Travelling with the screen locked sends **nothing** to these services.
- **Ground elevation is no longer looked up over the internet.** The terrain height used to calculate height above ground ("flight height") now comes from an elevation grid shipped inside the App. Your coordinates are **not** sent to any service for this, and the previous **Open-Meteo** elevation request has been removed.
- When you view the map, your approximate location (as map-tile coordinates) is sent to the **OpenStreetMap tile servers** to display map imagery.
- If you tap the Map tab's **fuel (Petrol/Gas)**, **Food**, **Hospital** or **Attractions** buttons, your coordinates and chosen search radius are sent to the **Overpass API** (an OpenStreetMap community service) to find nearby fuel stations, restaurants, medical services and attractions.
    - **Changed in version 1.18.0 — famous places no longer involve the internet.** The well-known attractions layer (temples, monuments, museums and the like) now comes from a list of notable places shipped **inside the App**, so it is worked out entirely on your device. Your coordinates are **no longer sent to the Wikidata Query Service** for this. The App still asks the **Overpass API** for the smaller, more local places around you, and for their exact positions.
    - The only exception: if that shipped list cannot be read on your device — for example there is not enough free storage — the App falls back to the previous **Wikidata Query Service** request so that you still see something. This is a failure path, not normal operation.
    - **Putting attractions in a sensible order does still involve Wikidata, and version 1.18.2 reduces it.** For places OpenStreetMap tags with a Wikidata identifier, the App may ask the **Wikidata Query Service** for information it uses to decide the order attractions are listed in. Until version 1.18.2 that was a request on most attraction searches. It sends **those place identifiers and your IP address — not your coordinates**. From version 1.18.2 the App answers most of them from the list shipped inside it, so a search around a well-known place typically sends nothing for this at all; only identifiers the shipped list does not hold are still looked up. Answers are remembered on your device for 30 days, so the same places are not asked about again.
- **The Map tab's new 🏛 Landmarks button (version 1.18.0) sends nothing at all.** Universities, stadiums and international airports are answered entirely from a list included in the App, so tapping it makes **no request to anyone** — it works with no signal, and in aeroplane mode. Unlike every other button on that row, it never contacts the Overpass API or any other service.
    - **Changed in version 1.17.0 — this now sends less.** Results of a search are remembered on your device, so looking again at somewhere you have already searched sends **nothing at all**: no coordinates, no request, and it works with no connection. See "nearby-places cache" under Data Storage for how long that lasts. Separately, the app now contacts **one** of these shared servers at a time rather than racing several, so a single search costs the services that donate them far less than it used to.
    - **Changed in version 1.15.0.** When those shared servers are overloaded, the App now tells you so after about 45 seconds instead of leaving you watching a spinner — but **the request itself stays open in the background for up to about 75 seconds**, in case a slow server still answers. If it does, the results simply appear. Nothing additional is sent, and no new request is made: it is the same single request, allowed to finish. Leaving the Map tab or starting another search ends it.
- **Attractions are looked up in advance, before you ask for them.** Because these searches are slow, the App starts looking for nearby attractions automatically — when you open the Map tab, when you move the map to a new place (by typing in the search box or by long-pressing a point), when you change the search distance, and again if you travel far enough that the previous results no longer describe where you are. This sends exactly the same thing as tapping **Attractions** would: your coordinates and the selected search radius to the **Overpass API**, and nothing else. **From version 1.18.0 the famous-places half of that advance lookup sends nothing at all**, because it is answered from the list inside the App. **Fuel and Food are not searched in advance** — those run only when you tap them. If you would rather nothing was sent, leave the Map tab; these lookups happen only while you are on it.
- If you **tap a place on the map**, the App works out its address using your device's **built-in geocoder** only, falling back to the on-device list of places when that has nothing. Only the tapped coordinates are shared with the device geocoder, solely for this purpose. Nothing is sent to Nominatim.
- If you type a place into the Map tab's **search box** (a ZIP code, city and state, landmark or address), that text is sent to your device's **built-in geocoder** and, if it finds nothing, to **Nominatim (OpenStreetMap)**, solely to turn it into a point on the map. Your approximate location is sent with it only so that nearby matches are ranked first. This happens only when you run a search; the text you type is not stored by the App or sent anywhere else.
- The same search box also finds **businesses by name** ("Walmart"), **kinds of place** ("grocery stores", "pharmacy") and **airports by code** ("LAX"). A business name goes to **Nominatim** along with your approximate location, so the nearest branches can be listed first; a kind of place and an airport code go to the **Overpass API** with your coordinates. As above, nothing is stored by the App, and searching "my location" is answered entirely on your device and sends nothing at all.
- **Typing in the search box is now the only thing in the App that can send your coordinates to Nominatim**, it happens only when you deliberately run a search, and it is limited to **20 searches per day per device**.
- If you tap the **"You are here" pin**, the App shows your address using your device's **built-in geocoder**, or the on-device list of places when that has nothing. This happens only when you tap the pin, and nothing is sent to Nominatim.
- Speed, trip distance, and altitude are derived on-device from the GPS signal and are not transmitted anywhere.
- The compass heading is derived on-device from the phone's motion (magnetometer) sensors. It is never transmitted.
- Step counts (and the calorie/distance estimates derived from them) come from your phone's step sensor and accelerometer, are computed on-device, and are never transmitted.
- **Trip history stays on your device.** To power the Trips tab, the App keeps a log of your recent journeys (coordinates, place names, and times) **in the App's private storage on your device only**, for your **7 most recent travel days**: a day's trips are deleted automatically once 7 newer days with travel have been recorded (days you don't travel don't shorten this). **You can also choose to keep individual trips indefinitely** by tapping the bookmark on them (up to 30 trips) — a kept trip is exempt from that automatic deletion and remains on your device until **you** delete it, or you uninstall the App. Nothing is kept indefinitely unless you ask for it: every trip is deleted automatically unless you have marked it yourself. This history is **never transmitted** to us or to any third party (viewing a route on the map only fetches map imagery, as above), and it is removed entirely if you uninstall the App. All other location data is held in memory only during active use and is discarded when tracking stops or the app is closed.

## Background Location
- The App offers two **optional**, separately controlled features that use location while the screen is locked or the app is in the background. Both are off until you turn them on, both run as an Android **foreground service** with an **ongoing, visible notification** so you always know when they are active, and both can be stopped at any time:
  - **Keep running in background** — keeps updating and announcing your location continuously until you switch it off.
  - **Trip recording** — saves your walks and drives to the on-device Trips tab, tracing each journey's route even while the phone is locked or in your pocket. It runs only after you have confirmed it (a one-time prompt on your first trip, or by turning the Trip recording switch on yourself), and it never announces or geocodes anything.
    - **Changed in version 1.14.0 — please read.** The screen-locked part used to start and stop with each journey. It now stays running for as long as the Trip recording switch is **on**, with its ongoing notification visible the whole time. Between journeys it checks your position at low accuracy about **once a minute**, purely to notice when a journey has begun; **full-accuracy GPS runs only while you are actually travelling**. This was necessary because Android does not allow an app like this one to *start* location tracking from the background — so an app that stopped between trips could not restart itself when you drove off, and journeys were being missed or recorded as a straight line between two points. The notification tells you which state it is in: *"Watching for your next trip"* or *"Recording your trip"*.
    - **The App does NOT request Android's "Allow all the time" background-location permission.** Location is granted to it **only while it is in use**, and that limit is deliberate. The practical consequence is stated plainly because it affects your recorded routes: a journey that begins while your phone is *already* locked cannot start tracing on its own, and may be recorded as a straight line from wherever the phone was last seen. Starting a journey with the App open — or with Trip recording already running — records it in full.
    - The Location group in Settings links to Android's **battery optimisation** screen. This is a convenience shortcut only: the App requests no special battery permission, and exempting it simply stops Android delaying location updates while the screen is off, which on some phones distorts a recorded route. Nothing about what is collected, stored or transmitted changes either way.
    - What has **not** changed: the positions collected between journeys are used only to decide whether a trip has started, they are held in memory and discarded, they are never written to your trip history unless a journey is actually recorded, and nothing is transmitted anywhere.
    - One switch controls all trip recording — in Settings, at the top of the Trips tab, or by long-pressing the Trips tab — and switching it off stops the service, the notification and all of its GPS use entirely.
- Background location is used **only** to provide the App's core features you enabled — live location, address, voice announcements, and on-device trip recording (routes, speed and distance). It is **never** used for advertising, profiling, or shared with third parties beyond the reverse-geocoding and weather services listed below, which receive only coordinates. Trip routes recorded in the background stay in the same on-device trip history described above (your 7 most recent travel days, plus any trips you have chosen to keep) and are never transmitted.
- Background location updates occur only while one of these features is enabled, and stop when it stops.

## Your Own Copies — Backup, Restore and Sharing
**Backup and restore are new in version 1.16.0; sharing and saving a single trip are new in version 1.17.0. Please read, because this is the one part of the App where your data can leave the protection of your phone, and only you can decide that.**

Until this version, trip history could not be got out of the App at all: changing phone, resetting it, or simply reinstalling destroyed every recorded journey, with no way to bring it back. The App now lets you make your own copies. **The App still never uploads anything, and we still have no servers and receive nothing** — but a copy you create is yours to look after, and what happens to it afterwards is outside the App's control.

- **Back up (Settings → Backup).** Writes your trips, their routes and your step history to a single file, **at a location you choose** through Android's own file picker — your Downloads, an SD card, or a cloud drive such as Google Drive. The App has no storage permission and never sees where you put it. If you choose a cloud folder, that file is then held by that cloud provider under **their** privacy policy, not this one.
- **Restore (Settings → Backup).** Reads a file you select and adds its trips to this phone. Journeys already present are left untouched, so nothing is overwritten.
- **Share a trip (⋮ menu on any trip).** Hands one journey to whichever app you pick from Android's share sheet — as a picture of the route, or as a **GPX**, **KML** or **JSON** file containing that journey's coordinates, place names and times. Whoever receives it can see everywhere that journey went.
- **Save a trip (⋮ menu on any trip).** The same journey data written to a location you choose, as above.
- **Nothing leaves your phone until you choose a destination.** No backup, file or picture is created or sent in the background, on a schedule, or without you asking for it.
- **A copy you have made is not covered by the App's own deletion.** Uninstalling the App, or clearing its data, removes everything inside the App — but it cannot reach a file you saved elsewhere or a trip you have already sent to somebody. Those remain until **you** delete them, wherever you put them. **Treat a backup file as you would a diary of where you have been.**

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
| Device geocoder (Google Play services) | Street address (reverse geocoding); place search — primary (only when you use the Map search box) | Lat/Lon coordinates; the place text you type | https://policies.google.com/privacy |
| **On-device place list (GeoNames, CC BY 4.0)** | Town/city/region/country name when there is no connection or the device geocoder has nothing | **Nothing — the data ships inside the App and never leaves your device** | https://www.geonames.org/ |
| **On-device elevation grid** | Ground elevation for "flight height" | **Nothing — the data ships inside the App and never leaves your device** | — |
| Nominatim (OpenStreetMap) | **Place search and business-name search only** — when you type in the Map search box, capped at 20 per day. **No longer used for reverse geocoding.** | Lat/Lon coordinates, IP; the place or business text you type | https://osmfoundation.org/wiki/Privacy_Policy |
| OpenStreetMap tile servers | Map display | Approximate location (tile coords), IP | https://osmfoundation.org/wiki/Privacy_Policy |
| Overpass API (OpenStreetMap community) | Nearby fuel stations, restaurants, medical services & local attractions; searches for a kind of place ("grocery stores") and airport codes. **The Landmarks button does not use this service, or any other.** Fuel, Food and Hospital only when you tap them; attractions also searched automatically in advance while you are on the Map tab (see "Location Data"). **The famous-places half of an attractions search no longer uses any service** — see version 1.18.0 above | Lat/Lon coordinates + search radius, IP; the kind of place or airport code you type | https://osmfoundation.org/wiki/Privacy_Policy |
| Wikidata Query Service (Wikimedia) | **Two uses, both reduced.** (a) *Finding* famous/notable attractions — **fallback only since version 1.18.0**: normally answered from a list shipped inside the App, and contacted only if that list cannot be read on your device. (b) *Ordering* them, for attractions OpenStreetMap tags with a Wikidata identifier. **Reduced in version 1.18.2**, which answers most of these from the shipped list; answers are then kept on your device for 30 days | (a) Lat/Lon coordinates, IP. (b) Wikidata place identifiers, IP — **not your coordinates** | https://foundation.wikimedia.org/wiki/Policy:Privacy_policy |
| OpenWeatherMap | Weather data | Lat/Lon coordinates, IP | https://openweather.co.uk/privacy-policy |
| Open-Meteo | Weather data (fallback only — **no longer used for elevation**) | Lat/Lon coordinates, IP | https://open-meteo.com/en/terms |
| Google Play In-App Updates | App updates | None (system-level) | https://policies.google.com/privacy |
| Google Play In-App Review | User ratings | None (system-level) | https://policies.google.com/privacy |
| Aptabase (EU-hosted) | Anonymous usage statistics | Anonymous event counts + app version, Android version, device model, country/locale — **no identifiers, no location** | https://aptabase.com/legal/privacy |

When you tap **Share** on the Location tab, the App builds a Google Maps link with your coordinates and hands it to whichever app you choose to share with. Sharing or saving a **trip** works the same way, but carries that journey's whole route rather than a single point — see "Your Own Copies" above. In both cases nothing is shared until you select a destination, and the App sends nothing to us or to any service of ours in the process.

## Advertising
The current version of the App does **not** display advertisements. Future versions may include ads served by Google AdMob. If ads are introduced, this privacy policy will be updated accordingly, and AdMob's data practices will apply (https://policies.google.com/technologies/ads).

## Permissions
| Permission | Purpose |
|-----------|---------|
| ACCESS_FINE_LOCATION | Determine precise GPS position for location, speed, and altitude |
| ACCESS_COARSE_LOCATION | Fallback network-based location |
| INTERNET | Fetch weather, map imagery, and the results of searches you run (place names and ground elevation no longer need it) |
| FOREGROUND_SERVICE | Run optional background location tracking |
| FOREGROUND_SERVICE_LOCATION | Declare the background service as a location service (Android 14+) |
| POST_NOTIFICATIONS | Show the ongoing tracking notification (Android 13+) |
| ACTIVITY_RECOGNITION | Count steps for the Speed tab's step counter, and — while trip recording is on — notice when you start moving so a trip can begin even if the phone was locked before you left (optional — Android 10+; denying it only disables step counting and this automatic start) |
| ACCESS_NETWORK_STATE | Let the map check for connectivity before fetching tiles |
| RECEIVE_BOOT_COMPLETED | Re-enable that automatic trip start after the phone restarts, if trip recording is on |

## Data Storage
- Location data written to storage by the App is limited to three things, all in the App's private storage, all never transmitted, and all removed on uninstall:
  - the **on-device trip history** described above — auto-deleted past your 7 most recent travel days unless you have chosen to keep a particular trip;
  - the **place cache** — coordinates and address text for places already looked up, so the same street is not looked up twice. Capped at 15,000 entries and each entry auto-deleted after 14 days; and
  - the **nearby-places cache** (new in version 1.17.0) — the results of Map searches you have run, kept so that returning to somewhere you have already looked does not have to ask the internet again. It holds the places found and the point you searched from, for up to **7 days** for attractions and **24 hours** once fuel, food or hospitals are included, capped at 32 searches. It is never transmitted.
- **Files you create yourself are the exception, and are not in the App's private storage.** A backup file, or a trip you have saved or shared, sits wherever you chose to put it — see "Your Own Copies" above. The App cannot read, manage or delete it afterwards, and uninstalling does not remove it.
- The App also stores non-personal app preferences on-device: a days-of-use counter (for the review prompt), the voice-announcement on/off setting, the in-app voice volume level, the keep-screen-awake setting, the preferred speed unit (mph/km/h), the preferred temperature unit (°F/°C), your daily step count, the anonymous-usage-statistics on/off setting, and a counter of postponed app-update reminders.
- If you choose to enter your body weight (used only to estimate calories from your steps), it is stored on-device only and never leaves your phone.
- No personal information is collected by us.

## Data Retention
We operate no servers and retain **no user data of any kind** on our side. All data the App uses lives only on your device, with these retention periods:

| Data | Where it is kept | How long |
|------|------------------|----------|
| Trip history (routes, place names, times) | App's private on-device storage | Your **7 most recent travel days** — a day's trips are deleted once 7 newer travel days exist |
| Trips you chose to keep (bookmarked, max 30) | App's private on-device storage | **Until you delete them** — exempt from the automatic 7-day pruning, and never transmitted |
| Place cache (coordinates + address text for places already looked up) | App's private on-device storage | **14 days per entry**, max 15,000 entries — never transmitted |
| Nearby-places cache (Map search results + the point searched from) | App's private on-device storage | **7 days** for attractions, **24 hours** if fuel/food/hospitals are included; max 32 searches — never transmitted |
| Backups, and trips you saved or shared | **Wherever you chose to put them** — not the App's storage | **Until you delete them.** The App cannot reach them, and uninstalling does not remove them |
| Current location, address, weather, speed, altitude, compass | Device memory only | Discarded when tracking stops or the App closes |
| App preferences (units, voice settings, optional body weight, step count, usage counters) | App's private on-device storage | Until you delete them or uninstall the App |
| Anonymous usage statistics (event counts — no identifiers, no location) | Aptabase (EU) | Up to 5 years, in anonymous aggregate form only |

The third-party services listed above (geocoding, weather, map tiles, searches you run) receive coordinates transiently to answer each request; we do not control their retention, which is governed by their own privacy policies linked in the table above. Place names and ground elevation are worked out entirely on your device and involve no third party at all.

## Data Deletion
Because we never collect or store your data on any server, **there is no data for us to delete** — everything is on your device and under your control. You can delete it at any time:

- **Delete everything the App holds:** uninstall the App, or go to **Android Settings → Apps → Find My Location → Storage → Clear data**. This permanently removes the trip history, the place cache, the nearby-places cache, all preferences, and any stored weight.
- **⚠️ Copies you made yourself are not included, and you must delete them yourself.** If you have created a backup file, saved a trip, or shared one, that copy is wherever you put it — your Downloads, an SD card, a cloud drive, or another person's phone. The App has no way to reach it, and uninstalling will not remove it. Delete those files where they live, and remember that anything already sent to somebody else cannot be taken back.
- **Trip history** also prunes itself automatically: only your 7 most recent travel days are kept. Trips you have bookmarked to keep are the one exception — they stay until you delete them, and you can un-bookmark one at any time to hand it back to the automatic pruning. Before a day of trips is pruned, the Trips tab warns you which day is about to go, so nothing you wanted disappears without notice.
- **Anonymous usage statistics** contain no identifiers by design, so they cannot be traced back to you or your device — there is nothing personal in them to delete. You can stop them being counted at any time in **Settings → Privacy**.

If you have any questions or requests regarding your data, contact us at **playmine.support@gmail.com** and we will respond promptly.

## Data Sharing
We do not sell, trade, or share your data with any third party beyond the services described above, each of which receives only the coordinates needed to perform its function. **The App itself never shares a trip with anyone.** The one way a journey reaches another person or service is if **you** send it — through the backup, save or share actions described in "Your Own Copies" — and then only to the destination you pick, at the moment you pick it.

## Data Security & Handling
We handle the personal and sensitive data the App works with (your location) as follows:

- Location is processed **on your device**. Everything the App itself writes to disk — the trip history (your 7 most recent travel days, plus any trips you chose to keep), the place cache, the nearby-places cache, and your preferences — is stored in the App's **private, sandboxed storage**, which Android prevents other apps from reading. A backup or shared trip that **you** create is deliberately outside that sandbox, because the whole point of it is to survive the App being removed; from that moment its safety is in your hands.
- All network communications (weather, map tiles, and searches you run) use **HTTPS/TLS encryption** and carry only coordinates — never your name, contacts, identifiers, or anything else, because the App never has such information.
- **This version sends less than any before it.** Working out where you are — the place name shown on the Location tab, and the ground elevation behind "flight height" — used to require requests to outside services on a timer as you travelled. Both are now answered from data shipped inside the App, so travelling with the App open sends **nothing** for either.
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
