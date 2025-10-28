# SPACEAPP v3.0/v4.0/v4.2 — End-User Guide (README)

*Real-time satellite lookup and tracking with ~800 pre-searched objects across 5 categories.*

## Overview

SPACEAPP lets you browse curated satellites and pull real-time data with one click. It’s designed for fast lookup, learning, and light tracking — not heavy analytics.

Curated list (~800 satellites) across 5 categories:

* Special, Starlink, Science, Weather, GPS

* One-click details: pick a category → pick a satellite → see live data (or use the search bar to search for satellite names that are already in DB)

* Manual search by NORAD ID for satellites outside the curated set

* Two API modes to balance speed vs. efficiency (for v4.0 above only, see table below)


## Setup

1. Go to [n2yo.com](https://www.n2yo.com/) and Sign Up to get the API Key (the Code at the end of the user information page)

2. Open the app -> Go to Signup and past the API Key where prompted

3. When the Signup is complete, you can now just Login with your username and password and use the app without pasting the API Key again.

* The same process apply for other accounts, you can easily switch between API Keys just by Loging In and Out.


## Quick Start (After setup)

1. Open the app.

2. Choose a category (e.g., Science). A short description and a list of satellites will appear.

3. Click a satellite name to fetch and display live information.

4. Not in the list? Paste its NORAD ID into the search bar and hit Search.

5. Tooltips / (?) icons in the app explain fields as you hover.


## What Data You’ll See

For each satellite, SPACEAPP can show (where available):

* Name & NORAD ID

* Position (live)

* Orbit / TLE (raw)

* Speed

* Estimated time in space

* Additional field help is shown via the in-app tooltip / (?) icons.


## API Modes (Polling Interval)
* Please note that this section is just for SPACEAPP v4.0 and v4.2, v3.0 users can skip.

Pick the mode that fits your needs. Efficient Mode reduces API pressure; Non-efficient prioritizes responsiveness.

**Sats (N)**	**Mode**	        **Interval**	**Time to 1k/hr**
9	            Efficient	             8 s	        ~14.8 min
7	            Efficient	             8 s	        ~19.0 min
7	            Non-efficient	         3 s	        ~7.0 min
8	            Efficient	             8 s	        ~16.7 min
8	            Non-efficient	         3 s	        ~6.0 min
10	            Efficient	             8 s	        ~13.3 min
10	            Non-efficient	         3 s	        ~5.0 min

**Recommendations**

Use Efficient (8s) for normal browsing or low bandwidth.

Switch to Non-efficient (~3s) when you need faster refresh and accept higher API usage.


## Tips for Best Results

Prefer the curated categories first; they’re pre-checked for quality.

When searching by NORAD ID, copy it carefully from a reliable source.

If requests fail repeatedly, switch to Efficient mode / check Network connection / API limit and try again.


## Troubleshooting

No data / errors when clicking a satellite

* Check your internet and try Efficient mode.

* Update the satellite database if prompted.

App froze during update / first run

* Wait a minute; if it doesn’t recover, restart the app.

* If corruption is suspected, reinstall may be required.

Search returns nothing

* Confirm the NORAD ID (typos are common).

* That satellite may have decayed or changed identifiers.


## Privacy

SPACEAPP queries public satellite data sources. It **does not collect personal information beyond what is required for normal operation.**


## Support & Contact

Questions, feedback, or bug reports: *tanbinhvo.hcm@gmail.com*


## Credits

Vo Tan Binh (aka Henry Vo) — Original and solo developer of the entire system.


## Copyright / License

*© Vo Tan Binh. All rights reserved.*
*This software and its assets are protected by copyright. Redistribution or reuse of code, artwork, or data without permission is prohibited unless explicitly allowed by the author.*

## Most features are self-explained in the interface; this README only highlights key behaviors and safe-use notes. Enjoy exploring the sky with SPACEAPP!
