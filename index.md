# Privacy Policy for Find My Location

**Last updated:** June 10, 2026  
**Developer:** PlayMine  
**Package:** net.playmine.findmylocation

## Overview
Find My Location ("the App") is a utility that shows your current location, address, weather, travel speed, and altitude/flight height. We are committed to protecting your privacy.

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
- **No location history is stored.** Location data is held in memory only during active use and is discarded when tracking stops or the app is closed.

## Background Location
- The App offers an **optional** continuous tracking mode that keeps updating and announcing your location while the screen is locked or the app is in the background.
- When active, this runs as an Android **foreground service** with an **ongoing, visible notification**, so you always know tracking is on. You can stop it at any time.
- Background location is used **only** to provide the App's core feature you enabled — live location, address, and voice announcements. It is **never** used for advertising, profiling, or shared with third parties beyond the reverse-geocoding and weather services listed below, which receive only coordinates.
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

## Data Storage
- No location data is written to disk or persistent storage.
- The App stores only non-personal app preferences on-device in SharedPreferences: a launch counter (for the review prompt), the voice-announcement on/off setting, the keep-screen-awake setting, the preferred speed unit (mph/km/h), the preferred temperature unit (°F/°C), and a counter of postponed app-update reminders.
- No personal information is stored.

## Data Sharing
We do not sell, trade, or share your data with any third party beyond the services described above, each of which receives only the coordinates needed to perform its function.

## Data Security
All network communications use HTTPS/TLS encryption.

## Children's Privacy
The App does not knowingly collect data from children under 13. The App does not require account creation or personal information.

## Changes to This Policy
We may update this privacy policy from time to time. Changes will be reflected in the "Last updated" date above. Continued use of the App constitutes acceptance of the updated policy.

## Contact
If you have questions about this privacy policy, contact us at:  
📧 playmine.support@gmail.com

## Consent
By using Find My Location, you consent to this privacy policy.
