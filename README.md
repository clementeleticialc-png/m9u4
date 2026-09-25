# M9U4 — ArcGIS Online deliverables (South New Brighton / Southshore, Christchurch)

Produced 25 Sep 2026 in ArcGIS Online org `educacionesri` (user usuario19zigurat).

## Files in this folder
| File | What | Use |
|---|---|---|
| `M9U4_diagnosis_map.jpg` | 1924×1467 export of the web map (no UI) | Slide 2 |
| `M9U4_site_boundary.geojson` | One polygon, WGS84 — the spit from Bridge St to Southshore Reserve, estuary edge to Marine Parade | Forma: import as site/context |

## Items in ArcGIS Online (My Content → usuario19zigurat)
| Item | Type | ID |
|---|---|---|
| M9U4 South New Brighton Resilience Diagnosis | Web Map | 212c128785814c37bc92e706e7ed1db4 |
| M9U4 Diagnosis Map – South New Brighton (export) | Image (PNG, 2.4 MB) | d3a9a46f05104514a9681d3fd19b11df |
| M9U4 Site Boundary – South New Brighton (for Forma) | GeoJSON | 113e5329b2024855953d3a10293848b7 |
| M9U4 CCC High Flood Hazard Residential Overlay – SNB extract | GeoJSON (112 parcels) | 36eb1ac3e7dc4e218a7287a4bbe28a1a |
| Schools_10min_walk_EastChch | Hosted Feature Layer (analysis output) | in My Content |

Open the map: https://educacionesri.maps.arcgis.com/apps/mapviewer/index.html?webmap=212c128785814c37bc92e706e7ed1db4

## Layers in the web map (top → bottom)
1. **Schools — MoE directory (east Christchurch)** — Eagle GIS / Ministry of Education "NZ Schools Directory", filtered to 13 schools: `Add1_City='Christchurch' AND Add1_Suburb IN (New Brighton, North New Brighton, South New Brighton, Southshore, Bexley, Aranui, Wainoni, Parklands, Avondale, Burwood, Dallington, Shirley)`
2. **High Flood Hazard Residential Overlay (New Brighton/Southshore) — CCC District Plan** — purple outline. CCC `OpenData/DistrictPlanB/FeatureServer/29`. District Plan Rule 5.5.6.2 RD2: residential units in the High Flood Hazard Management Area. Names New Brighton, Southshore, Redcliffs explicitly.
3. **Flood Hazard High (1-in-500yr, risk to life) — CCC** — red. `DistrictPlanB/FeatureServer/25`. "Potentially susceptible to inundation during an extreme hydrological event (1 in 500 years), may pose a risk to life or property due to water velocity and/or depth."
4. **Flood Management Area (tidal/rainfall, SLR-vulnerable) — CCC** — orange. `DistrictPlanB/FeatureServer/30`. "Land prone to flooding as a result of major tidal or rainfall events and vulnerable to the effects of climate change as a result of rising sea levels."
5. **Flood Extent 50-year — CCC** — blue, **off by default** (street-level mesh, too dense for the slide; keep for appendix). `WaterCharacteristic/FeatureServer/2`.
6. **10-min walk catchment to school (13 east Chch schools)** — green. ArcGIS Online *Generate Travel Areas*, walking time, 10-min cutoff, overlap policy = overlap. **6.5 credits** (0.5/facility).

Source portal: https://opendata-christchurchcity.hub.arcgis.com (search "flooding").

## What the map shows (slide-2 sentence)
The 10-minute walk catchments stop at the red Flood Hazard High band. South New Brighton School's catchment is the only one that sits entirely inside the Flood Management Area, and the purple District Plan overlay marks the homes already designated high-hazard along the estuary edge.

## Priority challenge (slide 3 — proposed)
**Flood-severed access on a one-road-out spit.** Shock: coastal/estuary inundation. Stress: sea-level rise (CCC classifies the area SLR-vulnerable). Exposed group: residents inside the District Plan overlay + primary-school children whose walk catchment crosses the hazard band.

Indicators (threshold, owner):
- % of overlay dwellings within a 10-min walk of a school that does not cross Flood Hazard High — threshold: ≥80% — owner: CCC Community Board
- Number of independent road exits from the spit passable in a 1-in-100 tidal event — threshold: ≥2 — owner: CCC Transport / Waka Kotahi
- Minutes to reach Bridge St / Pages Rd junction from Southshore Reserve on foot — threshold: ≤15 — owner: Civil Defence (CDEM Canterbury)

## Honest gaps (slide 6)
- **Map Viewer AI assistant not enabled** by the Zigurat org admin, although the user privilege `portal:user:useAIAssistants` is granted. AI prompting was evidenced by an external assistant (Claude) driving the ArcGIS Online workflow through the browser — screenshot the conversation.
- **No NZ health-facility layer** available in ArcGIS Online; access measured to schools only.
- **Per-user credit cap 10** (org pool 2,273). Full-city walk catchment (139 schools, 69.5 credits) not run; scoped to the 13 eastern schools.
- Evacuation-route analysis (Closest Facility to exits) not run — would cost ~0.5 credit per route; ask coordinator for allocation if wanted.
- Flood Extent 50-year layer hidden for legibility, not because it's wrong.

## Credits
Used 6.5 of 10. Remaining 3.5.
