# HomeMatch

A renter-facing UI prototype for Bay Area housing search, recommendations, applications, decisions, and lease tracking.

## Open the prototype

Live demo: [HomeMatch on GitHub Pages](https://huangwanyi1024.github.io/homematch/)

Download `index.html` and open it in a modern browser. HTML, CSS, JavaScript, and reference photos are embedded in this single file. No build step or external dependencies are needed.

## Live filtering

There are 24 fictional Bay Area homes priced from $900 to $4,200. Filter changes immediately update the results, preference chips, and schematic map; no Apply step is required. Maximum rent is an inclusive ceiling. Move-in by shows only homes available on or before the selected date; leave it empty for any date. Every required amenity must be present. Travel estimates differ by destination and travel method. All criteria are combined.

Private, shared, and entire-place rooms are supported across apartments, houses, studios, and condos. Some combinations legitimately return no matches, with guidance to widen the search. The sample Richmond room is closed; enable Include closed listings to see it.

**Regression checks:** run `node filter-tests.cjs` with Node.js. The checks use only built-in modules and verify the HTML shipped in this repository. They cover price ceilings, all 32 amenity combinations, location, availability dates, property and room type, commute destination/method/limit, sorting, map synchronization, and live state updates.

## Features

- Search and filter fictional Bay Area listings, save homes, and explore a schematic map.
- Follow listing details → application → documents → review → submission → status.
- Student-friendly supporting documents without a salary requirement.
- Validation, duplicate prevention, session recovery, withdrawal, and reapplication.
- Simulated provider decisions and lease creation after agreement finalization.

Expand **Prototype controls** to fill sample details and simulate events.

## Scope

UI only. No backend or real rental submission. Data is stored in session state in the current browser tab. For predictable persistence, serve this file through a static web host; direct file access may limit browser storage. Reference photos come from Unsplash and do not depict the fictional addresses.
