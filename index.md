# Privacy Policy for Find My Location

**Last updated:** July 7, 2026  
**Developer:** PlayMine  
**Package:** net.playmine.findmylocation

## Overview
Find My Location ("the App") is a utility that shows your current location, address, weather, travel speed, altitude/flight height, and steps — and keeps a short, on-device-only log of your recent trips so you can view your travelled routes. We are committed to protecting your privacy.

## Data Collection
The App does **NOT** collect, store, or transmit any personal data to servers operated by us. We do not use analytics, tracking, or advertising SDKs that collect personal information. We do not require an account, sign-in, or any personal details.

## Location Data
- Your location is determined on-device using Google Play Services (GPS/network).
- To convert coordinates into a human-readable address (reverse geocoding), the App first uses your device's **built-in geocoder** (provided by Google Play services on most devices); if it cannot resolve a street-level address, coordinates are sent to **Nominatim (OpenStreetMap)** instead. In both cases only the coordinates are shared, solely for this purpose.
- Location coordinates are sent to **OpenWeatherMap** and/or **Open-Meteo** solely to fetch current weather conditions.
- Location coordinates are sent to **Open-Meteo** solely to look up terrain ground elevation, used to calculate height above ground ("flight height").
- When you view the map, your approximate location (as map-tile coordinates) is sent to the **OpenStreetMap tile servers** to display map imagery.
- Speed, trip distance, and altitude are derived on-device from the GPS signal and are not transmitted anywhere.
- The compass heading is derived on-device from the phone's motion sensors and, while you are moving, the GPS direction of travel. It is never transmitted.
- Step counts (and the calorie/distance estimates derived from them) come from your phone's step sensor and accelerometer, are computed on-device, and are never transmitted.
- **Trip history stays on your device.** To power the Trips tab, the App keeps a log of your recent journeys (coordinates, place names, and times) **in the App's private storage on your device only**, for up to **7 days**, after which it is deleted automatically. This history is **never transmitted** to us or to any third party (viewing a route on the map only fetches map imagery, as above), and it is removed entirely if you uninstall the App. All other location data is held in memory only during active use and is discarded when tracking stops or the app is closed.

## Background Location
- The App offers an **optional** continuous tracking mode that keeps updating and announcing your location while the screen is locked or the app is in the background.
- When active, this runs as an Android **foreground service** with an **ongoing, visible notification**, so you always know tracking is on. You can stop it at any time.
- Background location is used **only** to provide the App's core features you enabled — live location, address, voice announcements, and on-device trip recording (speed and distance). It is **never** used for advertising, profiling, or shared with third parties beyond the reverse-geocoding and weather services listed below, which receive only coordinates.
- Background location updates occur only while you have this mode enabled, and stop when you stop the service.

## Voice Announcements
- The App can read your current place name aloud using your device's built-in **on-device text-to-speech** engine.
- No audio, and no location text, is sent off the device for this feature.

## Third-Party Services
| Service | Purpose | Data Sent | Privacy Policy |
|---------|---------|-----------|---------------|
| Google Play Services | GPS / network location | None (on-device) | https://policies.google.com/privacy |
| Device geocoder (Google Play services) | Reverse geocoding (address) — primary | Lat/Lon coordinates | https://policies.google.com/privacy |
| Nominatim (OpenStreetMap) | Reverse geocoding (address) — fallback | Lat/Lon coordinates, IP | https://osmfoundation.org/wiki/Privacy_Policy |
| OpenStreetMap tile servers | Map display | Approximate location (tile coords), IP | https://osmfoundation.org/wiki/Privacy_Policy |
| OpenWeatherMap | Weather data | Lat/Lon coordinates, IP | https://openweather.co.uk/privacy-policy |
| Open-Meteo | Weather and ground-elevation data | Lat/Lon coordinates, IP | https://open-meteo.com/en/terms |
| Google Play In-App Updates | App updates | None (system-level) | https://policies.google.com/privacy |
| Google Play In-App Review | User ratings | None (system-level) | https://policies.google.com/privacy |

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
| ACTIVITY_RECOGNITION | Count steps for the Speed tab's step counter (optional — Android 10+; denying it only disables step counting) |
| ACCESS_NETWORK_STATE | Let the map check for connectivity before fetching tiles |

## Data Storage
- The only location data written to storage is the **on-device trip history** described above: kept in the App's private storage, auto-deleted after 7 days, never transmitted, and removed on uninstall.
- The App also stores non-personal app preferences on-device: a days-of-use counter (for the review prompt), the voice-announcement on/off setting, the in-app voice volume level, the keep-screen-awake setting, the preferred speed unit (mph/km/h), the preferred temperature unit (°F/°C), your daily step count, and a counter of postponed app-update reminders.
- If you choose to enter your body weight (used only to estimate calories from your steps), it is stored on-device only and never leaves your phone.
- No personal information is collected by us.

## Data Retention
We operate no servers and retain **no user data of any kind** on our side. All data the App uses lives only on your device, with these retention periods:

| Data | Where it is kept | How long |
|------|------------------|----------|
| Trip history (routes, place names, times) | App's private on-device storage | **7 days**, then deleted automatically |
| Current location, address, weather, speed, altitude, compass | Device memory only | Discarded when tracking stops or the App closes |
| App preferences (units, voice settings, optional body weight, step count, usage counters) | App's private on-device storage | Until you delete them or uninstall the App |

The third-party services listed above (geocoding, weather, elevation, map tiles) receive coordinates transiently to answer each request; we do not control their retention, which is governed by their own privacy policies linked in the table above.

## Data Deletion
Because we never collect or store your data on any server, **there is no data for us to delete** — everything is on your device and under your control. You can delete it at any time:

- **Delete everything instantly:** uninstall the App, or go to **Android Settings → Apps → Find My Location → Storage → Clear data**. This permanently removes the trip history, all preferences, and any stored weight — nothing survives anywhere else.
- **Trip history** also deletes itself automatically after 7 days.

If you have any questions or requests regarding your data, contact us at **playmine.support@gmail.com** and we will respond promptly.

## Data Sharing
We do not sell, trade, or share your data with any third party beyond the services described above, each of which receives only the coordinates needed to perform its function.

## Data Security & Handling
We handle the personal and sensitive data the App works with (your location) as follows:

- Location is processed **on your device**. The only data written to disk — the 7-day trip history and your preferences — is stored in the App's **private, sandboxed storage**, which Android prevents other apps from reading.
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
