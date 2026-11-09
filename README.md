# Newton Trips

Interactive map and trip data for Bluebikes bikeshare trips that start or end at a station in Newton, MA.

**Live map:** https://newtonbluebikes.github.io/Newton_trips/

A map of Boston College T trips is in a separate project: https://newtonbluebikes.github.io/BC_bluebikes/

## Files

| File | What it is |
|---|---|
| `index.html` | Interactive map of trips at all 16 Newton Bluebikes stations, with a menu to pick the station. Opens in any web browser. |
| `newton-bluebikes-trips-2025-01_to_2026-10.csv` | Every Bluebikes trip that started or ended at one of Newton's 16 stations, January 2025 – October 2026 (44,189 trips). |

## Stations

| Station | ID (for links) | Trips |
|---|---|---|
| Auburndale | `N32015` | 1,792 |
| Bacon St at Washington St | `N32003` | 3,209 |
| Beacon at Walnut | `N32012` | 2,153 |
| Boston College T | `N32009` | 16,627 |
| California at Chapel | `N32011` | 4,132 |
| Centre St at Commonwealth Ave | `N32018` | 1,893 |
| Centre St at Washington St | `N32000` | 2,550 |
| Newton Highlands T | `N32010` | 2,786 |
| Newton Library | `N32013` | 1,093 |
| Nonantum Library | `N32002` | 2,974 |
| Union St at Herrick Rd | `N32008` | 3,580 |
| Upper Falls Greenway Pettee Square | `K13452` | 285 |
| Washington St at Crafts St | `N32001` | 1,984 |
| Washington St at Walnut St | `N32014` | 3,473 |
| Watertown St at Albemarle Rd | `N32006` | 1,971 |
| West Newton | `N32005` | 2,082 |

Trips counts every trip that started or ended at the station, including round trips.

## Data sources

- **Trips:** Bluebikes system data, monthly trip history files, January 2025 – October 2026.
- **Stations:** Bluebikes station list (updated August 21, 2026), plus Upper Falls Greenway Pettee Square (station K13452), which opened August 26, 2026.
- **Basemap:** MassGIS town boundaries, open space and major hydrography; MassDOT roads; MassGIS MBTA rapid transit lines.

## Notes on the trip file

- Newton stations are identified by station ID: the 15 stations with IDs beginning `N3`, plus `K13452` (Upper Falls Greenway Pettee Square).
- Station `N32008` appears as "Langley Lot" in March–April 2025 and as "Union St at Herrick Rd" afterward; both are included.
- Added columns: `duration_min` (trip length in minutes), `month`, `trip_type` (within Newton, from Newton, to Newton), `start_in_newton`, `end_in_newton`.
- Bluebikes removes staff trips and trips under 60 seconds before publishing. 33 trips in this file last more than 24 hours and are likely bikes that weren't docked properly.
- The data does not identify riders, so trips by students or other groups can't be separated out.

## Notes on the map

- Pick a station from the menu. Lines connect that station to the station at the other end of each trip. Line thickness shows total trips, on the same scale for every filter.
- Filters: season (all, fall, winter, spring, summer), direction (both, leaving the station, arriving at the station) and bikes (all bikes or e-bikes only).
- The side panel includes summary statistics on e-bike use and an About this data section with sources and caveats.
- Round trips (started and ended at the same station) are shown as a dashed ring around the station.
- Seasons: fall = September–November, winter = December–February, spring = March–May, summer = June–August.
- Distances are straight-line miles from the selected station.
- Most Newton stations have no trips before early March 2025. Gaps in service, such as Newton Highlands T in late August to late September 2025, are noted on the map for each station.
- To link to one station, add its station ID to the address, for example https://newtonbluebikes.github.io/Newton_trips/#N32010 for Newton Highlands T.
